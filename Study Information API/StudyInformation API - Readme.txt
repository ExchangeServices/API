————————————————————————————————————————————————————————
STUDY INFORMATION API																					1
Version: 8.0.0
————————————————————————————————————————————————————————
1.0	Initial version

1.0.1	Following changes has been done:
	- instead of specifying a date interval when 
	getting a study plan or subject plan you now
	specify a date. "StartDate" and "EndDate" has 
	been replaced with "SearchDate".
	- the attribute "points" has been removed from
	CourseChoiceCourse.
	- added the possibility to import program 
	choices. 
	- added two new deviation values, "Replacement"
	and "Transformation"
	- added a new attribute called "replacedcourse"
	- changes related to program profile and
	vocational outcome

1.0.2	Following changes has been done:
	- renamed "replacedcourse" to "comment"
	- added "start", "end" and "group" to course 
	choice
	- renamed "continuous" to "continues"
	- added services for delta export of study plan

1.0.3	Following changes has been done:
	- added courselevel to studyplan courses

1.0.4	Following changes has been done:
	- final version of V1. Removed not implemented 
	parts from documentation

1.0.5	Following changes has been done:
	- Changed "Lifecare Exchange Services" to 
	"Lifecare Education API Services". 

1.0.6	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
  
2.0.1	Following changes has been done:
	- added reduced property for subjects 
	- removed IndividualChoice from subject.type

2.0.2	Following changes has been done:
	- added subjectcode property for studyplancourse

2.0.3	Following changes has been done:
	- added status property for studyplancourse 

2.0.4	Following changes has been done:
	- added subject type values 

2.0.5	Following changes has been done:
	- added english attributes for subject, course,
	vocationaloutcome and content 

2.0.6	Following changes has been done:
	- Changed "Lifecare Exchange Services" to 
	"Lifecare Education API Services". 

2.0.7	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".
  
3.0.0	Following changes has been done:
	- Created new version of the API.
	- Added properties
	- removed three elements
	  + vocationaloutcomeenglishname from program 
	  + englishname from studyplancourse
	  + contentinenglish from studyplancourse

3.0.1	Following changes has been done:
	- Added properties
	  + vocationaloutcomenameinenglish in program 
	  + nameinenglish in studyplancourse
	  + contentinenglish in studyplancourse
	  + nameinenglish in subjectplansubject
	  + contentinenglish in coursechoicecourse

3.0.2	Following changes has been done:
	- Added properties
	  + nameinenglish in program
	  + orientationinenglish in program

3.0.3	Following changes has been done:
	- Renamed values in studyplancoursetype
	  + IndividualChoice -> IndividualOptions
	  + ProgramCommon -> ProgrammeSpecificSubjects
	  + ProgramRecess -> ProgrammeSpecialisation
	  + UpperSecondarySchoolWork -> DiplomaProject
	  + UpperSecondarySchoolCommon -> UpperSecondarySubjects
	  + OrientationAndProgramRecess -> OrientationAndProgrammeSpecialisation
	- Added values to studyplancoursetype
	  + UpperSecondarySubjectsForStudentsWithLearningDisabilities
	  + AssessedCourseWork
	  + CommonSubjectsInFurtherEducation
	  + Profile
	  + Outcome
	  + DegreeProject

3.0.4 Following changes has been done:
	  + Added property recommededsubjectcode in subjectplansubject

3.0.5	Following changes has been done:
	- Changed "Lifecare Education API Services" to
	"Tieto Education APIs".

4.0.0 Following changes has been done:
	- Created new version of the API
	- Added a number of attrbutes to studyplan
	- Added support to export school choices for students
	- Added support to import school placements

4.0.1 Following changes has been done:
    - Added missing attribute "courses.id" in Produktinformation

5.0.0 Following changes has been done:
	- Created new version of the API
	- Added more info in export school choices for students

(version 6 and 7 are not released)

8.0.0 Following changes has been done:
  - Added properties educationcoursetypepoints, extent, assessmenttext, assessmentdate and assessment lock date in studyplancourse
  - Added property typeofschoolplacement in schoolchoicestudent when importing school choices and school transfers
  - Added endpoint GetCompulsorySchoolSchoolChoicePeriods to retrieve basic period information

(version 9 is not released)

10.0.0 Following changes has been done:
  - Added properties allocatedTime, allocatedExtraTime and hoursRemainingOffered in studyplancourse
  - Added property commentstopurposeofeducation in studytime

 

