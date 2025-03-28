﻿————————————————————————————————————————————————————————
PERSONNEL API																		
Version: 8.0.0
————————————————————————————————————————————————————————
1.0	Initial version, based on Employee API.
	Compared with the Employee API following 
	changes has been done:
	- Added the "teachingqualification" and 
	"title" to "employment". 
	- Added services for import of teaching
	qualification.

1.0.1	Following changes has been done:
	- Added status attribute for personnel
	- Added type of employment

1.0.2	Following changes has been done:
	- Changed type for privacy from string 
	to enum. 

1.0.3	Following changes has been done:
	- Added an attribute called "workarea"
	- Added delta services

1.0.4	Following changes has been done:
	- Added the attributes "change" and 
	"timestamp"
	- Updates related to teacher qualifications

1.0.5	Following changes has been done:
	- "title" is replaced with "titlecode" and 
	"titlename"
	- "workarea.type" is replaced with 
	"workarea.code" and "workarea.name"

1.0.6	Following changes has been done:
	- Changed "Lifecare Exchange Services" to 
	"Lifecare Education API Services". 

1.0.7	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".

2.0	Following changes has been done:
	- Added support for middle name

2.0.1	Following changes has been done:
	- Added id on employment
	- Added attributes for contactinformation

2.0.2	Following changes has been done:
	- Updated schema with teacher qualification structure
	- Updated Tech Spec with teacher qualification info
	- Updated Produkt Info with teacher qualification info

2.0.3	Following changes has been done:
	- Updated domain model in Tech Spec

2.0.4	Following changes has been done:
	- Added possibility to read one personnel with PersonId

2.0.5	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".

3.0 	Following changes has been done:
	- Added support import of employments
	- For Norway only
	- For Compulsory School only

4.0 	Following changes has been done:
	- changed name for <unit> to <place>
	- added percent, titlecode and titlename to <placement>

5.0 	Following changes has been done:
	- added parameter UpdateAllPersonalInfo to service UpdatePersonInfo
	- added email2 to <employment>

All versions
	Following changes has been done for all versions:
	- Two new filtering parameters have been added for Complete export
	  - MunicipalityCode
	  - GovernedBy

6.0     Following changes has been done:
	- The privacy field for persons has changed type
	- Endpoint UpdateEmployments has replaced UpdatePersonInfo and UpdateEmploymentInfo
	- Endpoint UpdateEmployments is enabled for Swedish customers also

All versions:
    Following changes has been done for all versions:
    - Two new filtering parameters have been added for Delta export
      - MunicipalityCode
      - GovernedBy

8.0     Following changes has been done:
	- Endpoint UpdateEmployments is enabled for Finnish customers also
	- Endpoint UpdateEmployments is enabled for all school types

8.1     Following changes has been done:
	- Improved documentation regarding employments, i e specification of which attribues on entities that are mandatory at import.
