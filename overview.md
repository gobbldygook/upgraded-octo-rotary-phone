# Frontends
- gobbldygook.cli
    - load_area # -> AreaOfStudy
    - load_course # -> Course
- gobbldygook.web
    - load_area # -> AreaOfStudy
    - load_course # -> Course
- gobbldygook.lib

# The logic
- gobbldygook.core
    - expand_student # -> ExpandedStudent
- gobbldygook.core.schedule_builder
- gobbldygook.core.search_queries
- gobbldygook.core.student_format
- gobbldygook.core.course_conficts
- gobbldygook.core.examine
    - examine # -> ExaminationResults

# The area of study format
- hanson_format
    - prepare # -> AreaOfStudy

# … school-specific data?
- gobbldygook.school.stolaf
    - .deptnums  # deptnum-related functions, such as buildDeptNum
    - .data  # stuff related to st. olaf courses, such as valid departments, instructors, and times
    - .terms  # the toPrettyTerm, expandYear, and semesterName functions
    - .import_student  # functions to parse the SIS courses page into gobbldygook courses
        - import_student # -> BaseStudent

# random package that's part of stodevx and irrelevant to gobbldygook
- stolaf_sis_time_parser

