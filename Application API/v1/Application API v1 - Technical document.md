
<div style = " float : left;" align = "left">
<left>

   **Tieto Education APIs**

Application API
</left>



</div>
 <div style = " float : right;" align = "right">

<img src="../../Shared/Images/Edlevo%20White%20on%20HB@2x-80.jpg" alt="Edlevo" width="100"/>

Version 1.0.0

2025-02-20

</div>



<div style = " margin-top : 500px;margin-bottom : 500px;" align = "center">

# Technical Specification API
## Application API  

</div>



[comment]: # (Page break)
<div style="page-break-after: always;"></div>
<div style = " margin-top : 100px;">

## **Table of Contents**



[**1 Introduction**](#introduction)

- [**1.1 Prerequisites**](#prerequisites) 

[**2 Supported school types**](#supported-school-types)

[**3 Application API**](#application-api)

- [**3.1 Domain model**](#dm) 

- [**3.2 Entities**](#entities)
  
  -   [**3.2.1 Applicant Document**](#applicant-document)
     
[**4 Services**](#services)

- [**4.1 Update Applicant Document Service**](#update-applicant-document-service) 

<br/>  

</div>


[comment]: # (Page break)
<div style="page-break-after: always;"></div>
<div style = " margin-top : 100px;">

<div id ="introduction">

## **1 Introduction**

</div>

The Application API provides a service that makes it possible to update documents for applicants to the Edlevo application. The service in the Application API are accessed via URIs.

This document describes the following:

- What types of applicant documents that user can store via the Application API.
- How the information elements are structured

<div id ="prerequisites">

---

### **1.1 Prerequisites**

</div>

Before you can get access of the Application API, you must request a license key from TietoEvry. You should have basic knowlege on Swedish school system and W3C XML before you start using the API.

<br/>

</div>


<div style = "margin-bottom : 50px;">
</div>

[comment]: # (Page break)
<div style="page-break-after: always;"></div>
<div style = " margin-top : 100px;">

<div id = "supported-school-types">

## 2 Supported school types

</div>

<br/>

This API handles application documents for Adult School Types.


</div>

<div style = "margin-bottom : 50px;">
</div>

[comment]: # (Page break)
<div style="page-break-after: always;"></div>
<div style = " margin-top : 100px;">

<div id = "application-api">

## 3 Application

</div>

<div id = "dm">

 ### **3.1 Domain model**

</div>


This chapter describe the Application entities and their attributes.

<div style = "margin-top : 50px;">

![<](../../Shared/Images/Application-v1.png)

</div>

<div id = "entities" style = "margin-top : 50px">

### **3.2 Entities**

</div>
<div id = "applicant-document">

#### **3.2.1 Applicant Document** 

</div>

Attributes for applicant document attributes.

| Name                               | Description                             | Read-only |
| ---------------------------------- | --------------------------------------- | --------- |
| applicantid                        | SSN for the applicant                   | N         |
| schooltype                         | The school type for the applicant  <br/> Following types are defined <ul>KV (KomVux)</ul> <ul>SV (SärVux)</ul> <ul>SF (Svenska för invandrare)</ul> <ul>YH (Yrkeshögskola)</ul>      | N         |
| typeofdocument                     | Type of document to be stored <br/> Following types are defined <ul>ApplicationAppendix</ul> <ul>IKE_In</ul> <ul>IKE_Out</ul> | N         |
| filename                           | Name of the file to be stored           | N         |
| filecontent                        | Content of the file as a Base64 encoded string | N         |

<br/>

<br />


[comment]: # (Page break)
<div style="page-break-after: always;"></div>
<div style ="margin-top : 100px">
</div>

<div id="services">

## 4 Services

</div>

All services are based on HTTP REST technology. "Get services" are using the method HTTP GET. "Update services" are using the method HTTP POST.

<br/>

<div id="update-applicant-document-service">

### **4.1 Update Applicant Document Service**

</div>

This service stores a document for an applicant.
The maximum size of a file is 22MB.

If Edlevo already contains a document for the person with the same school type, document type and file name, that document is overwritten by the file content in the request.

A successful storing of the document returns an HTTP 200 statuc code.

Any validation error of the input returns an HTTP 400 status code.

Other types of errors returns an HTTP 500 status code.

**Services :**

| Service| Description|
| ------ | ---------- |
|UpdateAdultApplicantDocument| Save a document for an adult applicant.|

<br/>

