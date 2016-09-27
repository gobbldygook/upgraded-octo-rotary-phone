# student-format

## Api

### `encodeStudent`
Given a student object, returns a URL-formatted stringified version of it.

### `filterAreaList`
> If there's only one Physics major, then anyone can see and choose it. Otherwise, if there are more than one, then the list gets culled.

> The newest revision of a major is always available, unless the `available through` key is set.

> You can only enroll in a major if there isn't a newer one, unless your class year is between the previous one and the newest.

Given a list of area objects and a graduation year, filters the list to only those areas that can be used by the graduation year.

### `findCourseWarnings`
Given a schedule, analyzes the schedule for problems. Time conflicts, courses in the wrong year, and courses in the wrong semester.

### `isCurrentSemester`
Given a year, semester, and schedule, returns `true` if the schedule matches the (year,semester) pair.

### `schedule`
Schedule manipulation functions.

### `sortStudiesByType`
Given a list of areas, return the list sorted by type, in this order: 'degree', 'major', 'concentration', 'emphasis'.

### `student`
Student manipulation functions.

### `validateSchedule`
Given a schedule, checks various things to validate the schedule.

### `validateSchedules`
… I don't think this function needs to exist in here any longer.
