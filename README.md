# Gobbldygook

Hypothetical repositories:

### cli / web
Frontends.

### core
Brings together a bunch of packages.

### course-conflicts / examine-student / expand-student / schedule-builder / search-queries / student-format
Pacakges that try to do one task.

### hanson-format
The parser for the hanson format.

### lib
Miscallaneous packages that have no particular tie to gobbldygook.


## Example

Here's an example cli built with these hypothetical packages:

```ts
import {examine, expand_student} from '@gobbldygook/core'
import {loadCourse} from './load-course'
import {loadArea} from './load-area'
import * as fs from 'fs'
import * as school from '@gobbldygook/school-stolaf'

function prettify(school, results) {
    // make the results pretty
}

function main(student_file) {
    const student = fs.readFileSync(student_file, 'utf-8')

    // We start with a basic student, and flesh it out with the referenced data
    const loaded = expand_student(student, loadCourse, loadArea)

    // Then we check it
    const results = examine(loaded)

    // and finally we show the results
    print(prettify(school, results))
}
```
