————————————————————————————————————————————————————————
ORGANIZATION API																					1
Version: 1.0.1
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
 

