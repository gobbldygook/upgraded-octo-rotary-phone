# library functions

These will slowly be broken out into their own packages, most likely.

## `compare-props`
```ts
compareProps(a: ReactProps, b: ReactProps): boolean
```

Given two props from a React component, return `true` if they do _not_ match. Allows this to be easily used in `shouldComponentUpdate`.


## `errors`
```ts
class AuthError extends Error {}
class NetworkError extends Error {}
```

Errors.


## `fetch-helpers`
```ts
status(res: Response): Response | throws Error
classifyFetchErrors(err: Error): void | throws NetworkError
json(res: Response): Object  // calls the .json() method
text(res: Response): string  // calls the .text() method
```

Helpers for `window.fetch()`


## `find-missing-number-binary-search`
```ts
findMissingNumberBinarySearch(arr: number[]): number|void
```

Given an array of sequential numbers, find the first gap.


## `find-word-for-progress`
```ts
type ProgressChunk =
	'hundred' | 'ninety' | 'eighty' | 'seventy' |
	'sixty' | 'fifty' | 'forty' | 'thirty' |
	'twenty' | 'ten' | 'under-ten' | 'zero'
findWordForProgress(max: number, current: number): ProgressChunk
```

Given what is essentially a percentage, turn that into a word representing the percentage.


## `interpose`
```ts
interpose(data: any[], value: any): any[]
```

Given an array `[1, 2, 3]` and a value `'a'`, `interpose` returns a new array with the value interposed between each item in the original array `[1, 'a', 2, 'a', 3]`.


## `partition-by-index`
```ts
partitionByIndex(arr: any[]): [any[], any[]]
```

Partitions the given array by index: even indices are returned in the first array, and odd indices are returned in the second.


## `random-char`
```ts
randomChar(): string
```

Returns a random character from `[a-z]`.


## `split-paragraph`
```ts
splitParagraph(str: string): string
```

Given a paragraph, return an aray of the words within.


## `stringify-error`
```ts
stringifyError(err: Error, replacer: any, space: string|number): string
```

Essentially calls `JSON.stringify` on the error.


## `to-12-hour-time`
```ts
to12HourTime(time: string): string
```

Given a 24-hour time, such as 1300, return a formatted 12-hour time, 1:00pm. The 24-hour time must not contain colons.


## `zip-to-object-with-arrays`
```ts
zipToObjectWithArrays(keys: string[], vals: any[]): {[key: string]: any[]}
```

Like [_.zipObject][zipObject], except that every value will be wrapped in an array, and the values of duplicate keys will be joined together in the array.
