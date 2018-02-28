————————————————————————————————————————————————————————
OUTCOME API																					1
Version: 3.0.8
————————————————————————————————————————————————————————
1.0	Initial version

1.0.1	Following changes has been done:
	- Removed extended and corrected from 
	  CourseGrade
	- Removed extended and corrected from 
	  CourseReportGrade
	- Removed corrected from SubjectGrade
	- Removed corrected from SubjectReportGrade
	- Added date to SubjectGrade
	- Renamed referstofinalgrade to finalgrade for 
	  SubjectGrade and SubjectReportGrade
	- Added period to SubjectReportGrade
	- Renamed coursereportgrade to grades in the 
	  reports
	- Renamed subjectreportgrade to grades in the 
	  reports
	- Changed some properties from string to 
	  boolean
	- Removed assessor from Report
	
1.0.2	Following changes has been done:
	- Updated description of person id format
	
1.0.3	Following changes has been done:
	- Added groupid to coursegrade
	- Moved unit from gradeoutcome to coursegrade
	and subjectgrade

1.0.4   Following changes has been done:
	- Added courselevel to report grades
	- Added basiceligibility to reports
	
1.0.5	Following changes has been done:
	- Changed "Lifecare Exchange Services" to 
	"Lifecare Education API Services". 
	
1.0.6	Following changes has been done:
	- Clarified that when importing grades,
	old grades not mentioned in the input 
	are removed from BER. 

1.0.7	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 
2.0     Following changes has been done:
	- Added course assessments
	- Added subject assessments
	
2.0.1   Following changes has been done:
	- Changes input parameters to service for 
	getting national tests
	- Minor changes

2.0.2   Following changes has been done:
	- Removed period and semester from national
	tests. (Date should be sufficient.)
	
2.0.3	Following changes has been done:
	- Changed "Lifecare Exchange Services" to 
	"Lifecare Education API Services". 
	
2.0.4	Following changes has been done:
	- Updated with the gradeoutcome entity
	with the attribute 'complete'.
 
2.0.5	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 
3.0	Following changes has been done:
	- Added support for subtests for national tests
	- Added properties in the header
	
3.0.1	Following changes has been done:
	- Created gradeoutcome, subjectoutcome and nationaltestoutcome 
	
3.0.2	Following changes has been done:
	- Description of entities for national test results are updated
	- Added Use Cases for Import of National Test Results
	
3.0.3	Following changes has been done:
	- Updated schema for national test results
	- Updated documentation for national test results
	
3.0.4	Following changes has been done:
	- Updated Tech Spec documentation for national test results for courses
	- Updated schema file (changed cardinality for grades in national tests) 
	
3.0.5	Following changes has been done:
	- Updated Tech Spec documentation for subject grades / subject report grades
	- Updated Prod info documentation for subject grades / subject report grades
	- Updated schema file (added "semester" and "trialperformed") 
	
3.0.6	Following changes has been done:
	- Removed 'Omdöme i ämne' in Prod info documentation
	- Removed references to non-supported school types for Assessments in Tech Spec documentation
	
3.0.7	Following changes has been done:
	- Added property recommendedsubjectcode in subject
 
3.0.8	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
 

