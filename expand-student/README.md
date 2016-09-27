# expand-student

## Api

### `expandStudent`
```ts
expandStudent(student: Student, loadCourse: (clbid) -> Course, loadArea: ({name, revision, type}) -> AreaOfStudy): Promise<ExpandedStudent>
```

Given a student and two functions, returns a promise for the student to be fulfilled with data. This means that the schedules' lists of clbids should be expanded into lists of courses, and the studies' references to areas of studies should be fleshed-out into actual areas of study.
