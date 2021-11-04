<link rel="stylesheet" type="text/css" media="all" href="../../Shared/Styling/Custom.css" />

# Produktinformation 

## School Search API 

![<](../../Shared/Images/ApiGears.png)

School Search API är en programvara för att hantera skolvals- och skolbytesansökningar. Modulen ingår i plattformen Tieto Education APIs.  
 
Alla API’er levereras med en SDK som innehåller teknisk dokumentation och informationskontrakt som levereras via GitHub, https://github.com/ExchangeServices   

Modulen finns för grundskola.

<br />

### Informationsstruktur

Informationsstrukturen innehåller information rörande ansökningar.  

<br />

### Tekniska specifikationer 

School Search API använder tekniken XML och HTTP för informationsutbytet. 

<br />

## Dataspecifikationer 

### **Övergripande struktur som används av samtliga anrop.**

| Attribut               | Beskrivning                                         | Exempel |
| ---------------------- | --------------------------------------------------- | ------- |
| cityarea               | <a href="#Stadsdelsinfo">Information om en stadsdel</a> |     |
| school                 | <a href="#Skolinfo">Information om en skola</a>     |         |
| person                 | <a href="#Personinfo">Information om en person</a>  |         |
| configuration          | <a href="#Konfiginfo">Konfigurationsinformation</a> |         |
| child                  | <a href="#Elevinfo">Information om ett barn och dennes ansökningar</a> | |
| pdfdocument            | Antagningsbesked i pdf format                       |         |
| signature              | <a href="#signature">Information om godkännande av skolval/-byte</a> | |
| schooltextadmission    | Specifik text för en skola att visa hos e-tjänsten  |         |
| applicationnextyear    | <a href="#applicationnextyear">Ansökansinformation för skolval</a> | |
| applicationreelection  | <a href="#applicationbase">Ansökansinformation för reservansökan</a>    | |
| applicationcurrentyear | <a href="#applicationbase">Ansökansinformation för skolbyte</a> | |
| applicationnotapplying | <a href="#applicationnotapplying">Ansökansinformation för de som inte söker via denna tjänst</a> | |

<br />

<div id="Konfiginfo">

### **Konfiguration**

Konfigurationsspecifika attribut. Prefix för samtliga attribut är *configuration*.

| Attribut                           | Beskrivning                       | Exempel    |
 ----------------------------------- | --------------------------------- | ---------- |
| currentyearcutoffdate              | Övergångsdatum pågående läsår     | 2021-06-20 |
| currentyeardataupdate              | Återgångsdatum pågående läsår     | 2021-10-10 |
| currentyearapplicationson          | Ansökan nuvarande läsår aktiverad | true       |
| reelectionapplicationson           | Reservansökan aktiverad           | false      |
| birthyearforpreschoolclasschildren | Födelseår för förskoleklass       | 2015       |

</div>

<br />

<div id="Stadsdelsinfo">

### **Stadsdelsinformation**

Stadsdelsspecificka attribut. Prefix för samtliga attribut är *cityarea*.

| Attribut      | Beskrivning        | Exempel                                |
| ------------- | ------------------ | -------------------------------------- |
| areaid        | Id på stadsdel     | S10                                    |
| areaname      | Namn på stadsdel   | Östermalm                              |

</div>

<br />

<div id="Skolinfo">

### **Skolinformation**

Skolspecifika attribut. Prefix för samtliga attribut är *school*.

| Attribut          | Beskrivning                  | Exempel                   |
| ----------------- | ---------------------------- | ------------------------- |
| schoolid          | Id för skolan                | 3011                      |
| schoolname        | Namn på skolan               | Centralskolan             |
| schooltypeid      | Skolans regi (131 eller 132) | 131                       |
| isprofileschool   | Flagga för att visa om skolan har inriktningar | true    |
| profilename       | Namn på inriktningen         | Friluft Ur&Skur           |
| grade             | Lista på vilka årskurser som kan sökas | 7, 8, 9         |
| isschoolusingoursystem | Flagga som indikerar om skolan ingår i registrerat skolurval | true  |
| cityarea          | Stadsdelen skolan ligger i   |                           |
| proficiencytestid | Identitet på färdighetsprov  | BESPK                     |

</div>

<br />
<div id="Personinfo">

### **Personinformation**

Personspecifika attribut. Prefix för samtliga attribut är *person*.

| Attribut           | Beskrivning              | Exempel          |
| ------------------ | ------------------------ | ---------------- |
| ssn                | Personnummer             | 201212240123     |
| firstname          | Förnamn                  | Klas             |
| lastname           | Efternamn                | Andersson        |
| streetaddress      | Gatuadress               | Hemvägen 3       |
| zipcode            | Postnummer               | 12345            |
| postalarea         | Postadress               | Stockholm        |
| carofaddress       | C/O adress               |                  |
| protectedidentity  | Skyddad adress           | false            |
| notinmunicipality  | Boende utanför Stockholm | false            |

</div>

<br />


<div id="Elevinfo">

### **Elevinformation**

Elevspecifika attribut. Prefix för samtliga attribut är *child*. Listan av attribut inleds med de attribut som finns under <a href="#Personinformation">Personinformation</a>. Därefter kommer de nedanstående.

| Attribut                       | Beskrivning                             | Exempel |
| ------------------------------ | --------------------------------------- | ------- |
| applicationnextyear            | Skolvalsansökan för nästa år            | |
| applicationcurrentyear         | Skolbytesansökan för innevarande år     | |
| applicationreelection          | Reservansökan för nästa år              | |
| currentschool                  | Nuvarande skolplacering                 | |
| currentgrade                   | Nuvarande årskurs                       | 2       |
| hasappliedtonextyear           | Flagga om skolvalsansökan finns         | true    |
| hasappliedtocurrentyear        | Flagga om skolbyesansökan finns         | false   |
| hasappliedtoreelection         | Flagga om reservansökan finns           | false   |
| existsindatabase               | Flagga om eleven finns med i elevregistret | true |
| childproficiencytest           | Lista av färdighetsprov för eleven      |         |
| notapplying                    | Flagga om eleven ej söker skola         | false   |
| notappliedtonextyearreason     | <a href="#notapplyingtype">Anledning till att eleven avstår val</a> | None |
| notappliedtonextyearreasontext | Anledning till att eleven ej söker      |         |
| legalguardiancount             | Antal vårdnadshavare                    | 2       |

</div>

<br />

<div id="applicationbase">

### **Gemensam ansökningsinformation**

De attribut som är gemensamma för de tre olika ansökningstyperna. Skolbytes- och reservansökan har enbart dessa attribut, medan skolvalsansökan har ytterligare <a href="#applicationnextyear">attribut</a>. Prefix för samtliga attribut är *applicationcurrentyear* respektive *applicationreelection*.

| Attribut                    | Beskrivning                          | Exempel      |
| --------------------------- | ------------------------------------ | ------------ |
| childssn                    | Elevens personnummer                 | 201212240129 |
| applicationid               | Id på ansökan                        | {FB0AF286-CE53-463B-849D-F6886193C86E} |
| confirmationemail           | E-post                               | adam.bertil@hotmail.com |
| applicationtype             | <a href="#applicationtype">Typ av ansökan</a> | NextYear |
| legalguardian1signedssn     | Ansökande vårdnadshavarens personnummer  | 196212240129 |
| wantssiblingpriorityschool1 | Flagga för syskonförtur på skolval 1 | false        |
| wantssiblingpriorityschool2 | Flagga för syskonförtur på skolval 2 | false        |
| wantssiblingpriorityschool3 | Flagga för syskonförtur på skolval 3 | false        |
| phonenumber                 | Vårdnadshavarens mobilnummer         | 070070070    |
| phonenumberissecret         | Flagga om att mobilnumret är hemligt | false        |
| altphonenumber              | Alternativt telefonnummer            | 070070071    |
| altphonenumberissecret      | Flagga om att alternativa mobilnumret är hemligt   | false |
| updatedby                   | Uppdaterat av                        | 196212240129 |
| updatedat                   | Tidpunkt för senaste uppdatering av ansökan | 2021-05-07T00:00:00 |
| createdat                   | Tidpunkt för skapande av ansökan     | 2021-05-07T00:00:00 |
| lastupdated                 | Ej använd                            | |
| createdby                   | Skapad av                            | 196212240129 |
| firstschoolchoice           | Id på förstavalet av skola           | 3017         |
| secondschoolchoice          | Id på andravalet av skola            | 3018         |
| thirdschoolchoice           | Id på tredjevalet av skola           | 3019         |
| guaranteeschoolchoice       | Id på skolpliktsskola                | 3020         |
| firstschoolstatus           | <a href="#admissionstatustype">Status på ansökan</a> | NotAnswered |
| firstschoolname             | Namn på förstavalet av skola         | Sundskolan   |
| firstschoolnamewithgrades   | Namn på förstavalet av skola med valbar årskurs | Sundskolan-8 |
| firstschoolprofilename      | Namn på inriktning på förstavalet    | Friluft Ur&Skur |
| secondschoolstatus          | <a href="#admissionstatustype">Status på ansökan</a> | NotAnswered |
| secondschoolname            | Namn på andravalet av skola          | Dalskolan    |
| secondschoolnamewithgrades  | Namn på andravalet av skola med valbar årskurs | Dalskolan-8 |
| secondschoolprofilename     | Namn på inriktning på andravalet     |              |
| thirdschoolstatus           | <a href="#admissionstatustype">Status på ansökan</a> | NotAnswered |
| thirdschoolname             | Namn på tredjevalet av skola         | Bergskolan   |
| thirdschoolnamewithgrades   | Namn på tredjevalet av skola med valbar årskurs | Bergskolan-8 |
| thirdschoolprofilename      | Namn på inriktning på tredjevalet    |              |
| guaranteeschoolstatus       | <a href="#admissionstatustype">Status på ansökan</a> | Guarantee     |
| guaranteeschoolname         | Namn på skolpliktsskolan             | Planskolan   |
| guaranteeschoolnamewithgrades | Namn på skolpliktsskolan med valbar årskurs | Planskolan-8 |
| searchedgrade               | Sökt årskurs                         | 8            |

<br />
<div id="applicationnextyear">

### **Extra ansökningsinformation för skolval**

De attribut som tillkommer för skolval till nästa läsår. De gemensamma attributen ses <a href="#applicationbase">här</a>. Prefix för attributen - både dessa och de gemensamma - är *applicationnextyear*.

| Attribut                    | Beskrivning                  | Exempel       |
| --------------------------- | ---------------------------- | ------------- |
| notapplying                 | Flagga att eleven inte söker i denna skolvalsapplikation | false |
| notappliedreasonid          | <a href="#notapplyingtype">Anledning till att eleven ej söker</a> | None |
| notappliedtreason           | Anledning till att eleven ej söker   |  |
| hasappliedtootherschools    | Flagga att eleven har sökt till annan skola | false |
| otherschoolname             | Ej använd                    |  |
| wantssiblingpriorityschool4 | Flagga för syskonförtur på skolval 4 | false |
| wantssiblingpriorityschool5 | Flagga för syskonförtur på skolval 5 | false |
| fourthschoolchoice          | Id på fjärdevalet av skola   | 3018 |
| fifthschoolchoice           | Id på femtevalet av skola    | 3020 |
| fourthschoolstatus          | Status på ansökan, se <a href="#admissionstatustype">Status</a> | NotAnswered |
| fourthschoolname            | Namn på fjärdevalet av skola | Släntskolan |
| fourthschoolnamewithgrades  | Namn på fjärdevalet av skola med valbar årskurs | Släntskolan-8 |
| fifthschoolstatus           | Status på ansökan, se <a href="#admissionstatustype">Status</a> | NotAnswered |
| fifthschoolname             | Namn på femtevalet av skola          | Backeskolan |
| fifthschoolnamewithgrades   | Namn på femtevalet av skola med valbar årskurs  | Backeskolan-8 |

</div>

<br />

<div id="childproficiencytest">

### **Elevens färdighetsprov**

De attribut som beskriver elevens färdighetsprov. Prefix för attributen är *childproficiencytest*.

| Attribut           | Beskrivning                 | Exempel      |
| -------------------| ----------------------------| ------------ |
| childssn           | Elevens personnummer        | 201212240129 |
| proficiencytestid  | Färdighetsprovets id        | BESPK        |
| priorityorder      | Prioritetsordning på provet | 1            |

</div>
<br />

<div id="signature">

### **Signatur**

De attribut som beskriver en signatur. Prefix för attributen är *signature*.

| Attribut           | Beskrivning                      | Exempel      |
| -------------------| -------------------------------- | ------------ |
| childssn           | Elevens personnummer             | 201212240129 |
| legalguardianssn   | Vårdnadshavarens personnummer    | 196212240129 |
| legalguardianphonenumber | Vårdnadshavarens telefonnummer | 070070071 |
| acceptsschooloffer | Flagga om erbjudandet accepteras | true          |
| signaturephrase    | Signaturens data                 |              |
| signedat           | Tidpunkt för signering           | 2021-10-26T14:32:21 |
| otherschoolname    | Ej använd                        |  |
| otherschoolphonenumber | Ej använd                    |  |
| keepplaceinqueue   | Ej använd                        |  |
| applicationid      | Id på ansökan                    | {17084b40-08f5-4bcd-a739-c0d08c176bad} |
| numberoflegalguardians | Antalet vårdnadshavare till barnet | 2            |

</div>
<br />

<div id="applicationnotapplying">

### **Ej ansökan**

De attribut som beskriver elevens färdighetsprov. Prefix för attributen är *applicationnotapplying*.

| Attribut           | Beskrivning                 | Exempel      |
| -------------------| ----------------------------| ------------ |
| childid            | Elevens personnummer        | 201212240129 |
| reason             | Färdighetsprovets id        | BESPK        |
| reasontext         | Prioritetsordning på provet | 1            |
| createdby          | Skapad av                   | 196212240129 |

</div>
<br/>

### **Enumererade värden**

<br/>
<div id="admissionstatustype">

#### Status på ansökan

- NotAnswered
- Approved
- Guarantee
- GuaranteeRegret
- Declined 

</div>

<div id="applicationtype">

#### Typ av ansökan

- NextYear
- CurrentYear
- Reelection
- All

</div>

<div id="notapplyingtype">

#### Anledning till att inte ansöka

- None
- Unknown
- HasAppliedToSchoolInOtherMunicitality
- HasAppliedToIndependentSchool
- GradeSchoolNotWanted
- OtherReason

</div>

<br/>

### **Returvärden för samtliga anrop**

De attribut som beskriver elevens färdighetsprov. Prefix för attributen är *result*.

| Attribut           | Beskrivning                                 | Exempel   |
| -------------------| ------------------------------------------- | --------- |
| status             | Status på anropet, kan vara <ul><li>OK</li><li>ERROR</li></ul> | OK        |
| errormessage       | Lista av felmeddelanden, om status är ERROR |           |
---

