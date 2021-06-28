<style>
.alignright{
    float : right;
}

.alignleft{
    float : left;
}

.divsmall{
    margine-top : 200px;
}
</style>


<div class= "alignleft">
<left>

   **Tieto Education APIs**

Application Status API
</left>



</div>
 <div class= "alignright">

![alt](https://www.infopulse.com/files/images/evry-and-tieto-form-tietoevry-a-leading-nordic-digital-services-company-featured-image.jpg)

Version 1.0.0


</div>



<div style = " margin-top : 500px;margin-bottom : 500px;" align = "center">

# Technical Specification API
## Application Status API  

</div>


---
---

<div style = " margin-top : 20px;">

## **Table of Contents**



[**1 Introduction**](#introduction)

- [**1.1 Prerequisites**](#prerequisites) 

[**2 Supported school types**](#supported-school-types)

[**3 Application status API**](#applications-status-api)

- [**3.1 Domain model**](#dm) 

- [**3.2 Entities**](#entities)
  
  -   [**3.2.1 School choice and change**](#school-choice-change)
  -   [**3.2.2 Study choice**](#study-choice)
  -   [**3.2.3 Subject choice**](#subject-choice)
  -   [**3.2.4 Mother tongue educaiton**](#mte)
  -   [**3.2.5 Preschool leisure time center**](#plc)
     
  

</div>

<div id ="introduction" style = " margin-top : 100px;">

---
---

## **1 Introduction**

The Application status API provides services that makes possible to  integration with an external solution that presents status for ongoing applications within the school area,  together with status for application within other areas in the municipality. The service in the Application status API are accessed via URIs. Each of services has a unique URI.

This docuemnt descibes following:

- Which Application status information that user can get via the Application status API.
- How the Application status divided into entieties and how these entities are structured.

<div id ="prerequisites">

---
### 1.1 Prerequisites


Before you can get access tot he Application status API you must request a license key from TietoEvry. You should have basic knowlege on Swedish school system and W3C XML beofre you start using the API.

<br/>
<br/>

</div>

---
---

<div>

<div id = "supported-school-types" style = "margin-bottom : 50px;">

## Supported school types

<br/>


The table below descibes the supported types of school.
<br/>

| School type | Description | Code |
|-----------|:-----------:|-----------:|
|Compulsory Schoo|Compulsory school|GR|
|Upper Secondary School |Secondary school. 3-4 years education|GY|
|Preschool|Childcare for children between 1-6 years|FS|


</div>

---
---

<div id = "applications-status-api">

## 3 Applications status

<div id = "dm">

 - ### **3.1 Domain model**

</br>

This chapter describe the Application status entities  and their attributes.

<div style = "margin-top : 50px;">

![Applications stauts API domain model](./ASA.png)

</div>


</div>
</div>

<div id = "entities"style = "margin-top : 50px">

**3.2 Entities**

<div = style : "50px;">

<br />

## Data specifications 

Person attributes used by all applications.

**Note: All fields are read only**
<br>
| Attribut | Description                                         | Example                                |
| ---------- | --------------------------------------------------- | -------------------------------------- |
| id         | Uniq identifierare                                  | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| personid   | personnummer                                        | 19911201TF10                           |
| firstname  | First Name                                             | Nils                                   |
| middlename | Middle Name                                          | Larsson                                |
| lastname   | Last Name                                           | Persson                                |
| privacy    |Privacy protection for Student | level="2"                              |
 

 <br />

Application wise attributes. Prefixes for all attributes are: *application*.

| Attribut        | Description        | Example                                |
| --------------- | ------------------ | -------------------------------------- |
| id              | Unique identifier | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| period          | Period             | 20/21                                  |
| applicationdate | Date for application  | 2021-01-01                             |
| startdate       | Start date         | 2021-01-01                             |
| enddate         | end date          | 2021-05-15                             |
| status          | 	Status of school choice, school change and native language choice<br/> <br/>Status options are:<br/><br/> **School choice and change** <br/> - Utskickad <br/> - Påbörjad <br/> - Accepterad <br/> - Avböjd <br/> - Manuellt i inkorg <br/> - Oense <br/> - Flyttad till nya <br/> - Sparad <br/> - Maxpåminnelse ingen svarat <br/> - Maxpåminnelse en svarat <br/> - Hanterad <br/><br/> **Modersmålsval** <br/> - Beviljad <br/>- Kö <br/>- Beviljas <br/>- Avslås             | Hanterad  |
| unit            | Unit name         | Balderskolan                           |
| unitdomain      | School form           | Grundskola                             |

<br />
<div id = "school-choice-change">

## School choice and change

School choice and change specifiation attribute. Prefix for all attribut *schoolchoice*.

| Attribut      | Description        | Example                                |
| ------------- | ------------------ | -------------------------------------- |
| priority      | Priority        | 1                                      |
| id            | Unique identifier | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| placementarea | Placement area   | Östra                                  |
| unit          | Unit              | Balderskolan                           |
| grade         | Grade            | Skolår 2                               |
| incomingdate  | Incoming date    | 2021-01-01                             |

<br />
</div>

<div id = "val-av-inriktning">

## Study Choice

Specific attributes for targeting selection. Prefixes for all attributes are: *orientationchoice*.

| Attribut         | Description            | Example                                |
| ---------------- | ---------------------- | -------------------------------------- |
| educationplanid  | Education plan id | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| educationplan    | Education plan        | TEPRO20                                |
| program          | Program                | TEPRO                                  |
| schoolyear       | School year                 | 4                                      |
| classperiod      | Period                 | 20/21                                  |
| classid          | Class Id                | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| classname        | Class Name              | TE20                                   |
| timeofchoice     | Time of choice               | 2021-01-01                             |
| comment          | Comment              | Kommentar                              |
| coursetypeid     | Course type id             | INR                                    |
| coursetype       | Course type                | Inriktningar                           |
| priority         | Priority text              | 1                                      |
| status           | Status that can be: <br/>- Ansökt <br/>- Omval <br/>- Placerad                 | Placed                               |
| unitid           | Unit Id               | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| unitname         | Unit name             | Balderskolan                           |
| studyselectionid | Study selection Id             | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| schooldomain     | School form               | GY                                     |
| receipt          | Receipt               | 1                                      |
| id                          | Course Id                              | {17084b40-08f5-4bcd-a739-c0d08c176bad}           |
| priority                    | Priority Number                           | 1                                                |
| typeofchoice                | Type of choice                             | SPRAKVAL                                         |
| status                      | Status that can be: <br/>- Ansökt <br/>- Omval <br/>- Placerad                              | Ansökt                                           |
| periodforclass              | Class Period                         | 20/21                                            |
| classid                     | Class Id                             | {17084b40-08f5-4bcd-a739-c0d08c176bad}           |
| classname                   | Class name                           | TE19                                             |
| programcode                 | Program code                          | AHADM                                            |
| schoolyear                  | School year                              | 3                                                |
| coursename                  | Course name                            | Fysisk teater                                    |
| coursecode                  | Course code                             | TEAFYS0                                          |
| timeofchoice                | Time of choice                            | 2021-01-01                                       |
| startdate                   | Start date                          | 2021-01-01                                       |
| enddate                     | End date                           | 2022-01-01                                       |
| points                      | Points                               | 100                                              |
| unitdomainid                | Unit domain id                            | GY                                               |
| periodizededucationplanguid | Periodized education plan id | {17084b40-08f5-4bcd-a739-c0d08c176bad}           |
| unitguid                    | Unit guid                     | {17084b40-08f5-4bcd-a739-c0d08c176bad}                                                |
| unitid                      | Unit id                            | ACAD                                             |
| unitname                    | Unit name                          | Balderskolan                                     |
| periodid                    | Period Id                           | 20/21                                            |
| choiceperiodid              | Choice period id                  | 20/21                                            |
| receipt                     | Receipt                            | 1                                                |
| studyselectionguid          | Study selection id                    | {17084b40-08f5-4bcd-a739-c0d08c176bad}                                                 |
| schedulegroups              | Schedule grops                                    | Åk 3:2 |
| usplacementunitid           | Placement unit id                  | BLDR                                             |
| usplacementunitname         | Placement unit name                | Balderskolan  |
---
<br />
</div>
<div id = "subject choice">

## Subject choice

Subject choice specific attributes. Prefixes for all attributes are: *subjectchoice*.

| Attribut                | Description                          | Example                                                        |
 ----------------------- | ------------------------------------ | -------------------------------------------------------------- |
| id                      | Id                              | {17084b40-08f5-4bcd-a739-c0d08c176bad}                         |
| alternative             | Alternative                      |1                        |
| status                  |Status that can be:<br/> - Ny <br/>- Tilldelad <br/>   - Avvisad                               | Tilldelad |
| unitid                  | Unit id                             | 123                                                            |
| unitname                | Unit name                           | Balderskolan                                                   |
| unitdomainid            | Unit domain Id                          | 123                                                            |
| unitdomainname          | Unit domain name                        | Grundskola                                                     |
| areaid                  | Area Id                            | L3                                                             |
| periodid                | Period Id                            | 123                                                            |
| period                  | Period                               | 20/21                                                          |
| startdate               | Start date                           | 2021-01-01                                                     |
| enddate                 | End date                             | 2021-06-01                                                     |
| schoolyear              | School year                               | 5                                                              |
| subjecttypeid           | Ämnestypsid                          | 123                                                            |
| subjecttypename         | Subject Type name                        | Elevens val                                                    |
| subjectid               | Subject Id                              | 123                                                            |
| subjectname             | Subject name                            | Biologi                                                        |
| subjectabbreviation     | subject abbreviation                     | BI                                                             |
| guardiansubjectchoiceid | Guardian subject choice id | {17084b40-08f5-4bcd-a739-c0d08c176bad}                         |
---

</div>
<br />
<div  id = "mte">

## Mother tongue education 

Mother tongue education application specific attributes. Prefixes for all attributes are: *mothertongueeducation*.

| Attribut           | Description                                               | Example |
| ------------------ | --------------------------------------------------------- | ------- |
| subject            | Subject                                                      | Spanska
| unitdomain            | School form                                             | Grundskola
| unitmanagerid      | Unit manager Id | 19911201TF10                                             
| unitmanagername    | Unit manager name                                           | Karl Karlsson
| unitmanagerprivacy | Unit manager proteciton level | "level" = 2
| teacherid          | Teacher id | 19911201TF10                                                   |
| teachername        | Teacher name                                                 | Karl Karlsson
| teacherprivacy     |  Teacher proteciton level    | "level" = 2
---

<br />
</div>
<div id = "plc">

## Preschool and leisure time center
</br>

Preschool and leisure-Time center attributes. Prefixes for all attributes are: *preschoolleisuretimecenter*.

| Attribut                                          | Description                                                               | Example                                                  |
| --- | --- | --- |
| id                                                | Id                                                                | {17084b40-08f5-4bcd-a739-c0d08c176bad}                   |
| queuenumber                                       | Queue number                                                                   | 5                                                        |
| queuepriorityid                                   | Queue priority Id                                                           | 123                                                      |
| queueprioritytext                                 |  Queue priority text                                               | Uppehåll                                                 |
| prioritypoint                                     | Priority point                                      | 98                                                       |
| prioritypointgroup1                               | Priority point group 1                                      | 98                                                       |
| prioritypointgroup2                               |  Priority point group 2                                      | 98                                                       |
| prioritypointgroup3                               |  Priority point group 3                                      | 98                                                       |
| registereddate                                    | Registration date                                                     | 2021-01-01                                               |
| queuedate                                         | Queue date                                                                   | 2021-01-01                                               |
| placementrequestdate                              | Placement request date                                                              | 2021-01-01                                               |
| passivequeue                                      | Passie queue                                                                 | false                                                    |
| queueoptionid                                     | Queue option id                                                                  | 123                                                      |
| areaid                                            | Area id                                                                 | L3                                                       |
| placementarea                                     | Placement Area                                                          | Östra                                                    |
| unitid                                            | Unit id                                                                  | 123                                                      | S |
| unitname                                          | Unit name                                                                | Balderskolan                                             |
| childminderid                                     |Child minder id                                                | 19711201TF10                                             |
| childmindername                                   | Child minder name                                                        | Karin Larsson                                            |
| managementid                                      | Management Id                                                                      | 305                                                      |
| childactivitytype                                 | Child activity type                                                            | 123456                                                   |
| hassiblingwithplacement                           | Has sibling with placement         | true                                                     |
| hassiblingwithplacementinsamearea                 |Has sibling with placement in same area    | true                                                     |
| youngestsiblingbirthdate                          | Young establishing birth date | 2015-01-01                                               |
| oldestsiblingbirthdate                            | Old establishing birth date                                               | 2015-01-01                                               |
| youngestsiblingsbirthdateplacementinsamearea      | Young estsiblings birth date placement in same area | 2015-01-01                                               |
| Oldestsiblingsbirthdateplacementinsamearea        | Old estsiblings birth date placement in same area | 2015-01-01                                               |
| youngestsiblingsbirthdatequeueinsameunit          | young estsiblings birth date queue in same unit  | 2015-01-01                                               |
| oldestsiblingsbirthdatequeueinsameunit            | Old estsiblings birth date queue in same unit             | 2015-01-01                                               |
| youngestsiblingsbirthdatequeueinsamearea          | Young estsiblings birth date queue in same area                 | 2015-01-01                                               |
| oldestsiblingsbirthdatequeueinsame area            | Old estsiblings birth date queue in same area                | 2015-01-01                                               |
| oldestsiblingsbirthdatequeueorplacementinsamearea | Old estsiblings birth date queue or placement in same area| 2015-01-01                                               |
| oldestsiblingsbirthdatequeueorplacementinsameunit | Old estsiblings birth date queue or placement in same unit  | 2015-01-01                                               |
| hassiblinginqueue                                 |Has sibling in queue          | true                                                     |
| guaranteedate                                     | Guarantee date                                                              | 2021-01-01                                               |
| hasplacement                                      | Has placement                | true                                                     |
| hasplacementoffer                                 | Has placement offer                 | true                                                     |
| nativelanguagecode                                | Native languag ecode            | DEU                                                      |
| othernativelanguagecode                           | Other native language code            | ARA                                                      |
| nativelanguage                                    | Native language                                                    | Tyska                                                    |
| othernativelanguage                               | Other native language               | Arabiska                                                 |
| primaryadditionalinformationcode                  | Primary additional information code                 | 1234
| primaryadditionalinformationtext                  | Primary additional information text              | Behov av särskilt stöd
| carehours                                         | care hours                                                       | 40.0                                                     |
| extenttext                                        | Extent text        | Beskrivande text                                         |
| placementtypeid                                   |Placement type id                                                      | 123                                                      |
| placementtype                                     | Placement type                                                            | Parallell placering                                      |
| withinapplicationdeadline                         | Within application dead line           | true                                                     |
| guaranteemonth                                    | Guarantee month                                   | true                                                     |
| anychildminderinthearea                           | Any child minder in the area             | true                                                     |
| anyunitinthearea                                  | Any unit in the area         | true                                                     |


<br />
</div>
</div>
</div>

<div style ="margin-top : 50px">

## Services

</br>

All services are based on HTTP REST technology and organized in school types to match each school strcture. "Get services" are using the method HTTP GET.



</div>


<div>
**Services :**

| Service| Description|
---| ---|
|GetCompulsorySchoolChoiceApplications| Returns all compulsory school choice applications with  status for specific person identifier.|
GetCompulsorySchoolChangeApplications| Returns all compulsory school change applications with  status for specific person identifier.|
GetCompulsoryMotherTongueEducationApplications| Returns all mother tongue education applications status for specific person identifier.|
GetUpperSecondaryStudyChoiceApplications| Returns all Upper secondary study choice applications status for specific person identifier.|
GetSubjectChoiceApplications|Returns all subject choice applications status for specific person identifier.|
GetPreschoolLeisureTimeCenterApplication| Returns all perschool leisure time center applications for the specific person.


---
</div>
</br>
</br>

**Parameters :**

| Parameterx                                          | Mandatory                                                               | Description                                                  |
| --- | --- | --- |
PersonId| Yes| Person Id to search person's person id is specified and all applications will return if exist.
SearchDate|No| Specify search date to get all information with personId
---








