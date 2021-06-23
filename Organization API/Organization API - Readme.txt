————————————————————————————————————————————————————————
ORGANIZATION API
Version: 9.0.1
————————————————————————————————————————————————————————
1.0	Initial version

1.0.1	Following changes has been done:
 	- the sourcedid attribute "source" is now set to 
	the code for school type. 
	- personextension, groupextension and 
	membershipextension has been included in the 
	main XML schema. 
	- the XML schemas for personextension, 
	groupextension and membershipextension has been
	removed, which means that there is only one
	XML schema for the Organization API.
	- "grouptype.typevalue.level" is always set to 
	"1"
	- "member.role.status" is always set to "1", 
	which means that the member is active
	- the group extension attribute "period" has 
	been removed from class.
	- the person extension "populationkeycode" has 
	been renamed to "geographickeycode"
	- the person extensions "populationcityarea" 
	and "populationcityadmin" has been removed.
	- period type is now an enum type
	- added Years period
	- added subject code and subject name as 
	attributes for class
	- a new roletype ("Principal") has been added,
	for principals. 
	- added a new group extension called id.
	- changed name for the service parameter
	"SchoolUnitId" to "UnitId"
	- miscellaneous improvements in the 
	documentation
	- read-only columns for person and unit updated
 	- added schoolunitcode as membershipextension. 
	It is used in unit-principal relations
	- removed school type from sourcedid.source
	- removed schoolunitcode from "principal person"
	- added a person extension called "status"
	- changed restrictions for service parameters
	for dates.

 1.0.2	Following changes has been done:
	- added a new type of group called "MentorGroup"
	- the groupextension "schooltype" now contains
	all school types at unit.
	- added "programprofile" and "programvariant" as
	personextensions.
 	- updated delta export use cases.
	- updated description of person id format
	- updated organization exemple diagrams in
	technical specification.

1.0.3	Following changes has been done:
	- changed type for the membership extension 
	"schoolunitcode". "schoolunitcode" is now an
	array of strings.
	- updated "Examples of structures and mappings". 

1.0.4	Following changes has been done:
	- added description for "recstatus" for person, 
	group and membership.member.role.
	- removed group.description.long. 
	- removed group.extension.point.
	- added group.extension.hours.
	- updated "Delta export of organization"

1.0.5	Following changes has been done:
	- added membership role Responsible
	- excluded all preliminary placements
	- added schooltype in properties

1.0.6	Following changes has been done:
	- added mainunitname to groupextensions for units

1.0.7	Following changes has been done:
	- renamed mainunitname to officialunitname

1.0.8	Following changes has been done:
	- Changed "Lifecare Exchange Services" to 
	"Lifecare Education API Services". 

1.0.9	Following changes has been done:
	- Minor changes

1.0.10	Following changes has been done:
	- Documentation of delta export use cases

1.0.11	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 
2.0	Following changes has been done:
	- added services for creating/adding education groups
	- moved programcode, programprofile, programvariant 
	from person to membership 
	- removed employmentstart and employmentend from 
	person
	- added email address for units

2.0.1	Following changes has been done:
	- updated services for adding/updating education groups
	- added mainunitname for units

2.0.2	Following changes has been done:
	- changed name for services from "UpdateXXXEducationGroup"
	to "UpdateXXXGroup"

2.0.3	Following changes has been done:
	- renamed mainunitname to officialunitname 

2.0.4	Following changes has been done:
	- added new membership extension called hours, which 
	will be used in relation between teacher and group/class 

2.0.5	Following changes has been done:
    	- membership extensions grouped by relation type
	- added english name for course and subject

2.0.6	Following changes has been done:
    	- removed personextension "schoolunitcode"

2.0.7	Following changes has been done:
    	- removed english names for subjects and courses
	(they will be available in the Study Information API)
	- removed groupextensions "hours"
	(hours are available in relations)

2.0.8	Following changes has been done:
    	- added support for schedule groups
	- added a new attribute in relation between student
	and course. The attribute is called "cancelled"

2.0.9	Following changes has been done:
    	- added timeframe attribute in properties
	- the attribute properties/type is now an enum

2.0.10	Following changes has been done:
	- Changed "Lifecare Exchange Services" to 
	"Lifecare Education API Services". 

2.0.11	Following changes has been done:
	- Minor changes

2.0.12	Following changes has been done:
	- Documentation of delta export use cases

2.0.13	Following changes has been done:
	- Added points to course groups

2.0.14	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 
3.0	Following changes has been done:
	- Removed Course groups and Subject groups
	- Removed attribute signature and emailwork for teacher
	- Added list of responsibility, list of activity and placement to membershipextensions.
	- Moved attributes from membershipextension to responsibility, activity and placement.
	- Support for many placements in same class for a studnet
	- Support for many activities in same group for a studnet

3.0.1	Following changes has been done:
	- Changed placement to list of placements

3.0.2	Following changes has been done:
	- Added support for middlename 
 
3.0.3	Following changes has been done:
	- Added realestate to altadr
	- Added area as roletype for usage in municipal organization

3.0.4	Following changes has been done:
	- Updated use case documentation for delta
	- Updated what available delta functions exists

3.0.5	Following changes has been done:
	- Removed reference to service (delta for leisure time center) not supported in this version

3.0.6	Following changes has been done:
	- Added reference to service delta for leisure time center

3.0.7	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 
4.0	Following changes has been done:
	- Added vistingaddress for unit
	- Added resident status for person
	- Added integrated schooltype

4.0.1  	Following changes has been done:
	- SubjectCode and CourseCode removed from group extension

4.0.2  	Following changes has been done:
	- Added properties courseid and subjectid in activity extension in role

4.0.3	Following changes has been done:
	- Updated use case documentation for delta
	- Updated what available delta functions exists

4.0.4	Following changes has been done:
	- Updated use case documentation for delta 

4.0.5 	Following changes has been done:
    	- Added property recommededsubjectcode in activity extension in role

4.0.6	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 	

5.0	Following changes has been done:
	- Changed email to emailhome for person
	- Added emailworkschool to person
	- Added organizernumber to unit
	- Removed responsible role type
	- Added use of manager role type
	- Added group type ProfitCenter in municipal export
	- Unified calls for municipal export into one call for all school types

5.0.1	Following changes has been done:
    	- Added role type "Organization", and property type "MunicipalOrganization" in schema file
	- Added description of the Area and Organization group in Product Information
	- In Technical Specification:
	  + Updated pictures in ch 3.2
	  + Updated text about Municipal organization in ch 5 and 6.5
	  + Changes in description of Use Cases in ch 6.2.1

5.0.2	Following changes has been done:
    	- Added Use Case description for Department Groups

5.0.3	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 
5.0.4	Following changes has been done:
	- Added organizationtypecode for organizations
	- Added organizationtypename for organizations

6.0.0  Following changes has been done:
    - Added id in Period
    - Added vigonumber field in groupextension
    - Added gsinumber field in groupextension
    - Added organizationnumber field in groupextension
    - Added support for fetching teacher organization

7.0.0 Following changes has been done:
    - Added mentor element to membership extensions

7.0.1 Following changes has been done:
    - Removed PersonId argument for Get*Organization methods

7.0.2 Following changes has been done:
    - Updated structure examples for Compulsory and Upper Secondary School

8.0.0 Following changes has been done:
    - Added new group type: ExamGroup
    - Added new fields for group: subgrouptype and notes

9.0.0 Following changes has been done:
    - The privacy field for persons has changed type
    - A new field for units has been added - oidcode
    - A new field for units has been added - childactivitycode
    - A new field for groups has been added - profile
    - Endpoints for retrieving school placements added
    - Two new endpoints for teacher organization added

All versions 3 and up:
    Following changes has been done for all versions:
    - Two new filtering parameters have been added for Complete export
      - MunicipalityCode
      - GovernedBy
