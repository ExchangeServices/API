
 <style type='text/css'>
    img[alt$=">"] {
        float: right;
    }

    img[alt$="<"] {
        float: left;
        padding-right: 5px;
    }

    img[alt$="><"] {
        display: block;
        max-width: 100%;
        height: auto;
        margin: auto;
        float: none!important;
    }

    body {
        max-width: 40em;
    }

</style>
# Produktinformation #

## Application Status API ##

<br />

![<](Images/ApiGears.png)
Application Status API är en programvara för att hämta status gällande olika typer av ansökningar. Modulen ingår i plattformen Tieto Education APIs.  
 
Alla API’er levereras med en SDK som innehåller teknisk dokumentation och informationskontrakt som levereras via GitHub, https://github.com/ExchangeServices   

<br/><br/>
Modulen finns för skolformerna grundskola och gymnasieskola och tillhandahåller status för följande typer av ansökningar:

- Skolval
- Skolbyte
- Utbildning i modersmål
- Ämnesval

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
|privacy        |Sekretesskydd för personen <br/><br/>Om personen är skyddad, gäller följande värden på ”level”: <br/>1 &emsp;&emsp; Skyddad adress <br/>2 &emsp;&emsp; Skyddad folkbokföring <br/>3 &emsp;&emsp; Både 1 och 2 
|timestamp      |       
 
<br/>

Applikationsgemensamma attribut.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                  |-
|application.id                 |                   |
|application.period             |                   |
|application.applicationdate    |                   |
|application.startdate          |                   |
|application.enddate            |                   |
|application.status             |                   |
|application.unit               |                   |
|application.unitdomain         |                   |


<br />
Skolvalsspecificka attribut.

|Attribut                       |Beskrivning        |Exempel
|-                              |-                  |-
|priority                       |                   |
|id                             |                   |
|placementarea                  |                   |
|unit                           |                   |
|grade                          |                   |
|incomingdate                   |                   |