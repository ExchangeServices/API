————————————————————————————————————————————————————————
ORGANIZATION API																					1
Version: 2.0.9
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





