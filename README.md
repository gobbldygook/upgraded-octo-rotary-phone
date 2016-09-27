# Gobbldygook


Here's an example cli built with these hypothetical packages:

```ts
import {examine, expand_student} from '@gobbldygook/core'
import {load_course} from './load_course'
import {load_area} from './load_area'
import * as fs from 'fs'
import * as school from '@gobbldygook/school-stolaf'

function prettify(school, results) {
    // make the results pretty
}

function main(student_file) {
    const student = fs.readFileSync(student_file, 'utf-8')

    // We start with a basic student, and flesh it out with the referenced data
    const loaded = expand_student(student, load_course, load_area)

    // Then we check it
    const results = examine(loaded)

    // and finally we show the results
    print(prettify(school, results))
}
```
