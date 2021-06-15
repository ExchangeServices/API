
<style type='text/css'>
    img[alt$=>] {
        float: right;
    }

    img[alt$=<] {
        float: left;
        padding-right: 5px;
    }

    img[alt$=><] {
        display: block;
        max-width: 100%;
        height: auto;
        margin: auto;
        float: none!important;
    }

    body {
        max-width: none;
    }

</style>
# Produktinformation #

## Application Status API ##

<br />

![<](Images/ApiGears.png)
Application Status API är en programvara för att hämta status gällande olika typer av ansökningar. Modulen ingår i plattformen Tieto Education APIs.  
 
Alla API’er levereras med en SDK som innehåller teknisk dokumentation och informationskontrakt som levereras via GitHub, https://github.com/ExchangeServices   

<br />/><br />/>
Modulen finns för skolformerna förskola, grundskola och gymnasieskola. Modulen tillhandahåller status för följande typer av ansökningar:

- Skolval
- Skolbyte
- Val av inriktning
- Kurs- och ämnesval
- Modersmålsundervisning
- Val av förskola och fritids

<br />

### Informationsstruktur ###

Informationsstrukturen innehåller rörande kalenderaktiviteter.  

<br />

### Tekniska specifikationer ### 

Application Status API använder tekniken XML och HTTP för informationsutbytet. Tjänsterna är grupperade på skolform, filtreras på elev och kan även filtreras efter tidpunkt. 

<br />

## Dataspecifikationer ##

Huvudattribut.

|Attribut       |Beskrivning        |Exempel
|-              |-                  |-
|id             |                   
|personid       |Id för eleven
|firstname      |Förnamn för elev
|middlename     |Mellannamn för elev
|lastname       |Efternamn för elev
|privacy        |Sekretesskydd för personen <br /><br />Om personen är skyddad, gäller följande värden på ”level”: <br />1 &emsp;&emsp; Skyddad adress <br />2 &emsp;&emsp; Skyddad folkbokföring <br />3 &emsp;&emsp; Både 1 och 2 
|timestamp      |       
 
<br />

Applikationsgemensamma attribut. Prefix för samtliga attribut är *application*.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                  |-
|id                             |                   |
|period                         |                   |
|applicationdate                | Datum för ansökan |
|startdate                      | Startdatum        |
|enddate                        | Slutdatum         |
|status                         | Status            |
|unit                           | Skola             |
|unitdomain                     | Skolform          |


<br />

Skolvalsspecificka attribut. Prefix för samtliga attribut är *schoolchoice*.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                  |-
|priority                       | Prioritet         |
|id                             |                   |
|placementarea                  | Område            |
|unit                           | Skola             |
|grade                          |                   |
|incomingdate                   | Inkommandedatum   |

<br />
Skolbytesspecifika attribut. Prefix för samtliga attribut är *schoolexchange*?


<br />
Specifika attribut för val av inriktning. Prefix för samtliga attribut är *orientationchoice*.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                  |-
|educationplanid                |                   |                
|educationplan                  |                   |
|program                        | Program           |
|schoolyear                     | Skolår            |
|classperiod                    |                   |
|classid                        |                   |
|classname                      | Namn på klass     |
|timeofchoice                   |                   |
|comment                        | Kommentar         |
|coursetypeid                   |                   |
|coursetype                     |                   |
|priority                       | Prioritet         |
|status                         | Status            |
|unitid                         | Id på skola       |
|unitname                       | Namn på skola     |
|studyselectionid               |                   |
|schooldomain                   | Skolform          |
|receipt                        |                   |


<br />
Kursvalsspecifika attribut. Prefix för samtliga attribut är *coursechoice*.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                  |-
|id                             |                   |
|priority                       | Prioritet         |
|typeofchoice                   | Typ av val        |
|status                         | Status                  |
|periodforclass                 |                   |
|classid                        |                   |
|classname                      |                   |
|programcode                    |                   |
|schoolyear                     |                   |
|coursename                     |                   |
|coursecode                     |                   |
|coursepoints                   |                   |
|timeofchoice                   |                   |
|startdate                      |                   |
|enddate                        |                   |
|points                         |                   |
|unitdomainid                   |                   |
|periodizededucationplanguid    |                   |
|unitguid                       |                   |
|unitid                         |                   |
|unitmunicipalitycode           |                   |
|unitname                       |                   |
|periodid                       |                   |
|choiceperiodid                 |                   |
|receipt                        |                   |
|studyselectionguid             |                   |
|schedulegroups                 |                   |
|usplacementunitid              |                   |
|usplacementunitname            |                   |

<br />
Ämnesvalsspecifika attribut. Prefix för samtliga attribut är *subjectchoice*.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                  |-
|id                             |                   |
|alternative                    |                   |
|status                         |                   |
|unitid                         |                   |
|unitname                       |                   |
|unitdomainid                   |                   |
|unitdomainname                 |                   |
|areaid                         |                   |
|periodid                       |                   |
|period                         |                   |
|startdate                      |                   |
|enddate                        |                   |
|schoolyear                     |                   |
|subjecttypeid                  |                   |
|subjecttypename                |                   |
|subjectid                      |                   |
|subjectname                    |                   |
|subjectabbreviation            |                   |
|guardiansubjectchoiceid        |                   |

<br />
Modersmålsundervisningsspecifika attribut. Prefix för samtliga attribut är *mothertongueeducation*.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                                                          |-
|subject                        |                                                           |
|type                           |                                                           |
|unitmanagerid                  |                                                           |
|unitmanagername                |                                                           |
|unitmanagerprivacy             |                                                           |
|teacherid                      | Id på lärare                                              |
|teachername                    | Namn på lärare                                            |
|teacherprivacy                 | Sekretesskydd för läraren <br /><br />Om läraren är skyddad, gäller följande värden på ”level”: <br />1 &emsp;&emsp; Skyddad adress <br />2 &emsp;&emsp; Skyddad folkbokföring <br />3 &emsp;&emsp; Både 1 och 2                               |


<br />
Förskola- och fritidsspecifika attribut. Prefix för samtliga attribut är *preschoolleisuretimecenter*.

|Attribut                                           |Beskrivning        |Exempel
|-                                                  |-                  |-
|id                                                 |                   |
|queuenumber                                        | Köplats           |
|queuepriorityid                                    |                   |
|queueprioritytext                                  |                   |
|prioritypoint                                      |                   |
|prioritypointgroup1                                |                   |
|prioritypointgroup2                                |                   |
|prioritypointgroup3                                |                   |
|registereddate                                     |                   |
|queuedate                                          |                   |
|placementrequestdate                               |                   |
|passivequeue                                       |                   |
|queueoptionid                                      |                   |
|areaid                                             |                   |
|placementarea                                      |                   |
|unitid                                             | Id på skola       |
|unitname                                           | Namn på skola     |
|childminderid                                      |                   |
|childmindername                                    |                   |
|managementid                                       |                   |
|childactivitytype                                  |                   |
|hassiblingwithplacement                            |                   |
|hassiblingwithplacementinsamearea                  |                   |
|youngestsiblingbirthdate                           |                   |
|oldestsiblingbirthdate                             |                   |
|youngestsiblingsbirthdateplacementinsamearea       |                   |
|oldestsiblingsbirthdateplacementinsamearea         |                   |
|youngestsiblingsbirthdatequeueinsameunit           |                   |
|oldestsiblingsbirthdatequeueinsameunit             |                   |
|youngestsiblingsbirthdatequeueinsamearea           |                   |
|oldestsiblingsbirthdatequeueinsamearea             |                   |
|oldestsiblingsbirthdatequeueorplacementinsamearea  |                   |
|oldestsiblingsbirthdatequeueorplacementinsameunit  |                   |
|hassiblinginqueue                                  |                   |
|guaranteedate                                      |                   |
|hasplacement                                       |                   |
|hasplacementoffer                                  |                   |
|nativelanguagecode                                 |                   |
|othernativelanguagecode                            |                   |
|nativelanguage                                     |                   |
|othernativelanguage                                |                   |
|primaryadditionalinformationcode                   |                   |
|primaryadditionalinformationtext                   |                   |
|carehours                                          |                   |
|extenttext                                         |                   |
|siblingswithplacement                              |                   |
|placementtypeid                                    |                   |
|placementtype                                      |                   |
|withinapplicationdeadline                          |                   |
|placementrequestdateformatinyearmonth              |                   |
|guaranteemonth                                     |                   |
|anychildminderinthearea                            |                   |
|anyunitinthearea                                   |                   |
|extrainformation                                   |                   |