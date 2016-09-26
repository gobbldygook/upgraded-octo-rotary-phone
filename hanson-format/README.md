# hanson-format

The specification and parser for the "Hanson Format".

## Usage:

`npm install --save @gobbldygook/hanson-format`

```js
import {parse} from '@gobbldygook/hanson-format'

const data = `
name: A Major
type: major
revision: 2016-17
result: JAPAN 111
`

const result = parse(data)
console.log(result)

// result is now the following:/
result = {
	name: 'A Major',
	type: 'major',
	revision: '2016-17',
	result: {
		type: 'course',
		departments: ['JAPAN'],
		number: 111,
	}
}
```

---

This package also provides a cli for the hanson format, available through the `@gobbldygook/hanson-format-cli` npm package. It's used like `hanson-format area_of_study_file`, and it prints out the JSON representation of the area of study file.

---

To evaluate a student against an asrea of study file, use the `@gobbldygook/examine-student` package.
