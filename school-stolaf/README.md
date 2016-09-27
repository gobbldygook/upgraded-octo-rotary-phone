# school-stolaf

Encompasses everything that is unique to an individual school (I hope.)

## Deptnums
```
public buildCourseIdent  ; ok i'm honestly not sure why I have both this and buildDeptNum
public buildDeptNum  ; given a course-like object (matches {departments, number, section}), return a deptnum
public quacksLikeDeptNum  ; given a string, is it a deptnum?
public splitDeptNum  ; given a deptnum string, returns a {departments, number, section} dictionary
```

## Import
```
public importStudent  ; import a student from an online portal
private? getStudentInfo  ; actually do the import
private? convertStudent  ; normalizes the student
getSchedule  ; doesn't belong here; given a student, year, and semester, returns the active schedule for that year/semester pair
```

## … prettiness? (todo: better name)
```
public normalizeDepartment  ; given a "department", returns the uppercase departmental abbreviation
public normalizeGereq  ; um. hmm. given a g.e. requirement, returns the uppercased version of its name?
public expandYear  ; given a year, returns the school year variant (2012 => 2012-13)
public toPrettyTerm  ; given a term, expands the semester and year into their string forms
public semesterName  ; these need to be named consistently… given a semester number, returns the name
```

## Internal Data
```
private course_types  ; mapping of course type abbreviations to course types
private departments  ; mapping of department names to abbreviations
private gereqs  ; mapping of ge requirement names to abbreviations
```
