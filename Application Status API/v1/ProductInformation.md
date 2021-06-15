<link rel="stylesheet" type="text/css" media="all" href="ProductInformation.css" />

# Produktinformation #

## Application Status API ##

<br />

![<](Images/ApiGears.png)
Application Status API är en programvara för att hämta status gällande olika typer av ansökningar. Modulen ingår i plattformen Tieto Education APIs.  
 
Alla API’er levereras med en SDK som innehåller teknisk dokumentation och informationskontrakt som levereras via GitHub, https://github.com/ExchangeServices   

<br /><br />
Modulen finns för skolformerna förskola, grundenhet och gymnasieenhet. Modulen tillhandahåller status för följande typer av ansökningar:

- Skolval
- Skolbyte
- Val av inriktning
- Kurs- och ämnesval
- Modersmålsundervisning
- Val av förskola och fritids

<br />

### Informationsstruktur ###

Informationsstrukturen innehåller rörande ansökningar.  

<br />

### Tekniska specifikationer ### 

Application Status API använder tekniken XML och HTTP för informationsutbytet. Tjänsterna är grupperade på skolform, filtreras på elev och kan även filtreras efter tidpunkt. 

<br />

## Dataspecifikationer ##

Huvudattribut.

| Attribut   | Beskrivning                                   | Exempel |
| ---------- | --------------------------------------------- | ------- |
| id         |                                               |
| personid   | Id för elev                                   | {17084b40-08f5-4bcd-a739-c0d08c176bad}
| firstname  | Förnamn för elev                              |
| middlename | Mellannamn för elev                           |
| lastname   | Efternamn för elev                            |
| privacy    | <a href="#privacy">Sekretesskydd</a> för elev |
| timestamp  |                                               |
 
<br />

Applikationsgemensamma attribut. Prefix för samtliga attribut är *application*.

| Attribut        | Beskrivning       | Exempel |
| --------------- | ----------------- | ------- |
| id              |                   |
| period          |                   |
| applicationdate | Datum för ansökan |
| startdate       | Startdatum        |
| enddate         | Slutdatum         |
| status          | Status            |
| unit            | Enhet             |
| unitdomain      | Skolform          |


<br />

Skolvalsspecificka attribut. Prefix för samtliga attribut är *schoolchoice*.

| Attribut      | Beskrivning     | Exempel |
| ------------- | --------------- | ------- |
| priority      | Prioritet       |
| id            |                 | 
| placementarea | Område          |
| unit          | Enhet           |
| grade         | Betyg           |
| incomingdate  | Inkommandedatum |

<br />

<div class="red">Skolbytesspecifika attribut. Prefix för samtliga attribut är *schoolexchange*?</div>


<br />

Specifika attribut för val av inriktning. Prefix för samtliga attribut är *orientationchoice*.

| Attribut         | Beskrivning            | Exempel |
| ---------------- | ---------------------- | ------- |
| educationplanid  | Id för utbildningsplan |
| educationplan    | Utbildningsplan        |
| program          | Program                |
| schoolyear       | Skolår                 |
| classperiod      | Period                 |
| classid          | Klassid                |
| classname        | Klassnamn              |
| timeofchoice     | Valdatum               |
| comment          | Kommentar              |
| coursetypeid     | Kurstypsid             |
| coursetype       | Kurstyp                |
| priority         | Prioritet              |
| status           | Status                 |
| unitid           | Enhetsid               |
| unitname         | Enhetsnamn             |
| studyselectionid | Id för val             |
| schooldomain     | Skolform               |
| receipt          |                        |


<br />
Kursvalsspecifika attribut. Prefix för samtliga attribut är *coursechoice*.

| Attribut                    | Beskrivning                     | Exempel |
| --------------------------- | ------------------------------- | ------- |
| id                          |                                 |
| priority                    | Prioritet                       |
| typeofchoice                | Typ av val                      |
| status                      | Status                          |
| periodforclass              |                                 |
| classid                     | Klassid                         |
| classname                   | Klassnamn                       |
| programcode                 | Programkod                      |
| schoolyear                  | Skolår                          |
| coursename                  | Klassnamn                       |
| coursecode                  | Kurskod                         |
| coursepoints                | Kurspoäng                       |
| timeofchoice                |                                 |
| startdate                   | Stardatum                       |
| enddate                     | Slutdatum                       |
| points                      | Kurspoäng                       |
| unitdomainid                | Skolform                        |
| periodizededucationplanguid |                                 |
| unitguid                    | <div class="red">Enhetsid</div> |
| unitid                      | Enhetsid                        |
| unitmunicipalitycode        |                                 |
| unitname                    | Enhetsnamn                      |
| periodid                    | Id för period                   |
| choiceperiodid              | Id för vald period              |
| receipt                     |                                 |
| studyselectionguid          |                                 |
| schedulegroups              |                                 |
| usplacementunitid           |                                 |
| usplacementunitname         |                                 |

<br />
Ämnesvalsspecifika attribut. Prefix för samtliga attribut är *subjectchoice*.

| Attribut                | Beskrivning      | Exempel |
| ----------------------- | ---------------- | ------- |
| id                      | Ämnesid          |
| alternative             |                  |
| status                  | Status           |
| unitid                  | Enhetsid         |
| unitname                | Enhetsnamn       |
| unitdomainid            | Skolformsid      |
| unitdomainname          | Skolformsnamn    |
| areaid                  | Områdesid        |
| periodid                | Periodsid        |
| period                  | Period           |
| startdate               | Startdatum       |
| enddate                 | Slutdatum        |
| schoolyear              | Skolår           |
| subjecttypeid           | Ämnestypsid      |
| subjecttypename         | Ämnestypsnamn    |
| subjectid               | Ämnesid          |
| subjectname             | Ämnesnamn        |
| subjectabbreviation     | Ämnesförkortning |
| guardiansubjectchoiceid |                  |

<br />
Modersmålsundervisningsspecifika attribut. Prefix för samtliga attribut är *mothertongueeducation*.

| Attribut           | Beskrivning                                         | Exempel |
| ------------------ | --------------------------------------------------- | ------- |
| subject            | Ämne                                                |
| type               | Typ                                                 |
| unitmanagerid      | Id för enhetschef                                   |
| unitmanagername    | Namn för enhetschef                                 |
| unitmanagerprivacy | <a href="#privacy">Sekretesskydd</a> för enhetschef |
| teacherid          | Id på lärare                                        |
| teachername        | Namn på lärare                                      |
| teacherprivacy     | <a href="#privacy">Sekretessskydd</a> för lärare    |


<br />

Förskola- och fritidsspecifika attribut. Prefix för samtliga attribut är *preschoolleisuretimecenter*.

| Attribut                                          | Beskrivning           | Exempel |
| ------------------------------------------------- | --------------------- | ------- |
| id                                                |                       |
| queuenumber                                       | Köplats               |
| queuepriorityid                                   |                       |
| queueprioritytext                                 |                       |
| prioritypoint                                     |                       |
| prioritypointgroup1                               |                       |
| prioritypointgroup2                               |                       |
| prioritypointgroup3                               |                       |
| registereddate                                    |                       |
| queuedate                                         |                       |
| placementrequestdate                              |                       |
| passivequeue                                      |                       |
| queueoptionid                                     |                       |
| areaid                                            |                       |
| placementarea                                     |                       |
| unitid                                            | Enhetsid              |
| unitname                                          | Enhetsnamn            |
| childminderid                                     | Id för dagbarnvårdare |
| childmindername                                   |                       |
| managementid                                      |                       |
| childactivitytype                                 | Verksamhetskod        | 123456  |
| hassiblingwithplacement                           |                       |
| hassiblingwithplacementinsamearea                 |                       |
| youngestsiblingbirthdate                          |                       |
| oldestsiblingbirthdate                            |                       |
| youngestsiblingsbirthdateplacementinsamearea      |                       |
| oldestsiblingsbirthdateplacementinsamearea        |                       |
| youngestsiblingsbirthdatequeueinsameunit          |                       |
| oldestsiblingsbirthdatequeueinsameunit            |                       |
| youngestsiblingsbirthdatequeueinsamearea          |                       |
| oldestsiblingsbirthdatequeueinsamearea            |                       |
| oldestsiblingsbirthdatequeueorplacementinsamearea |                       |
| oldestsiblingsbirthdatequeueorplacementinsameunit |                       |
| hassiblinginqueue                                 |                       |
| guaranteedate                                     |                       |
| hasplacement                                      |                       |
| hasplacementoffer                                 |                       |
| nativelanguagecode                                |                       |
| othernativelanguagecode                           |                       |
| nativelanguage                                    |                       |
| othernativelanguage                               |                       |
| primaryadditionalinformationcode                  |                       |
| primaryadditionalinformationtext                  |                       |
| carehours                                         |                       |
| extenttext                                        |                       |
| siblingswithplacement                             |                       |
| placementtypeid                                   |                       |
| placementtype                                     |                       |
| withinapplicationdeadline                         |                       |
| placementrequestdateformatinyearmonth             |                       |
| guaranteemonth                                    |                       |
| anychildminderinthearea                           |                       |
| anyunitinthearea                                  |                       |
| extrainformation                                  |                       |

<br />

## Sekretesskydd ## 
<a name="privcy"></a>
Om personen är skyddad gäller följande värden på ”level”: <br />1 &emsp;&emsp; Skyddad adress <br />2 &emsp;&emsp; Skyddad folkbokföring <br />3 &emsp;&emsp; Både 1 och 2