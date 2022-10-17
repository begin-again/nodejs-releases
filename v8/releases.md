## Releases

Performance improvements and web assembly are not included.

[V8 Blog](https://v8.dev/blog), [Chrome Roadmap](https://chromestatus.com/roadmap), [Repository](https://chromium.googlesource.com/v8/v8.git/)

|                                                                                                                        |
| :--------------------------------------------------------------------------------------------------------------------- |
| [10.1](#101), [10.6](#106)                                                                                             |
| [9.0](#90), [9.1](#91), [9.2](#92), [9.3](#93), [9.4](#94), [9.5](#95), [9.6](#96), [9.9](#99), [9.9](#99)             |
| [8.0](#80), [8.1](#81), [8.4](#84), [8.5](#85), [8.6](#86), [8.7](#87), [8.8](#88), [8.9](#89)                         |
| [7.0](#70), [7.1](#71), [7.2](#72), [7.3](#73), [7.4](#74), [7.5](#75), [7.6](#76), [7.9](#79), [7.7](#77), [7.8](#78) |
| [6.0](#60), [6.1](#61), [6.2](#62), [6.3](#63), [6.4](#64), [6.5](#65), [6.6](#66), [6.7](#67), [6.8](#68), [6.9](#69) |
|                                                                                                                        |


## Highlights


### 10.6

<a href="#v106">

- [Intl.NumberFormat v3](https://github.com/tc39/proposal-intl-numberformat-v3)


### 10.1

<a href="#v101">


- [Array.prototype.findLast]() `[{a:1, b:2},{a:1, b:3}].findLast(o => o.a === 1) // { a: 1, b: 3 }` |



### 9.9

<a href="#v99">

[blog](https://v8.dev/blog/v8-release-99)

- new properties added to Intl.Locale
  - textInfo, `{ direction: 'rtl' }`
  - weekInfo, `{firstDay: 6, weekend: [5, 6], minimalDays: 1}`
  - calendars, collations, hourCycles, numberingSystems, timeZones
    - array of preferred identifiers of those in common use
- Intl.[supportedValuesOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/supportedValuesOf)



### 9.7

<a href="#97">

[blog](https://v8.dev/blog/v8-release-97)

- findLast and findLastIndex array methods
```js
[1,2,3,4].findLast( el => el % 2 === 0) // 4
[1,2,3,4].findLastIndex( el => el % 2 === 0) // 3
```


### 9.6

<a href="#v96">

[blog](https://v8.dev/blog/v8-release-96)


### 9.5

<a href="#v95">

[blog](https://v8.dev/blog/v8-release-95)<br>

- Intl.DisplayNames v2
  - added: calendar, dateTimeField
  - enhanced the support for the “language” type with a new languageDisplay option,
- Extended timeZoneName option
  - Intl.DateTimeFormat API in v9.5 now supports four new values for the timeZoneName option:
    - _shortGeneric_ to output the name of the time zone as in a short generic non-location format, such as “PT”, “ET”, without indicating whether it is under daylight saving time.
    - _longGeneric_ to output the name of the time zone as in a short generic non-location format, such as _Pacific Time_, _Mountain Time_, without indicating whether it is under daylight saving time.
    - _shortOffset_ to output the name of the time zone as in the short localized GMT format, such as _GMT-8_.
    - _longOffset_ to output the name of the time zone as in the long localized GMT format, such as “GMT-0800”.


### 9.4

<a href="#v94">

[blog](https://v8.dev/blog/v8-release-94)

- Class static initialization blocks

```js
class C {
  // This block will run when the class itself is evaluated
  static { console.log("C's static block"); }
}

```


### 9.3

<a href="#v93">

[blog](https://v8.dev/blog/v8-release-93)

- [object.hasOwn](https://v8.dev/features/object-has-own)
- [Error.cause](https://v8.dev/features/error-cause)


### 9.2

<a href="#v92">

[blog](https://v8.dev/blog/v8-release-92)

- [at method](https://v8.dev/features/at-method) is now available on Arrays, TypedArrays, and Strings. `[1,2,3].at(-1)` is 3
  - also available on FF 90


### 9.1

<a href="#v91">

[blog](https://v8.dev/blog/v8-release-91)

- [top-level await](https://v8.dev/features/top-level-await) enabled by default
- [Private brand checks]() enabled by default. Extends the [in operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/in) to also work with private field #-names


### 9.0

<a href="#v90">

[blog](https://v8.dev/blog/v8-release-90)

- [RegExp match indices](https://v8.dev/features/regexp-match-indices)

### 8.9

<a href="#v89">

[blog](https://v8.dev/blog/v8-release-89)

- [Top-level await](https://v8.dev/features/top-level-await)

### 8.8

<a href="#v88">

[blog](https://v8.dev/blog/non-backtracking-regexp)

- new experimental non-backtracking regular expression engine

### 8.7

<a href="#v87">

[blog](https://v8.dev/blog/v8-release-87)

- Atomics.waitAsync, [Atomics explainer](https://v8.dev/features/atomics)
- Unsafe Fast JS calls


### 8.6

<a href="#v86">

[blog](https://v8.dev/blog/v8-release-86)

- Open sourced JS-Fuzzer
- Speed-ups in Number.prototype.toString
- Atomics.wake renamed to Atomics.notify
- Anonymous classes now have a .name property whose value is the empty string ''
- The built-in Reflect object now has a Symbol.toStringTag property whose value is 'Reflect'



### 8.5

<a href="#v85">

[blog](https://v8.dev/blog/v8-release-85)

- [Promise.any and AggregateError](https://v8.dev/features/promise-combinators#promise.any)
- [String.prototype.replaceAll](https://v8.dev/features/string-replaceall)
- [Logical assignment operators](https://v8.dev/features/logical-assignment)
- Support for JS BigInts


### 8.4

<a href="#v84">

[blog](https://v8.dev/blog/v8-release-84)

- [Weak references and finalizers](https://v8.dev/features/weak-references)
- [Private methods and accessors](https://v8.dev/features/class-fields#private-class-fields)


### 8.1

<a href="#v81">

[blog](https://v8.dev/blog/v8-release-81)

- Intl.DisplayNames


## 8.0

<a href="#v80">

[blog](https://v8.dev/blog/v8-release-80)

- [optional chaining](https://v8.dev/features/optional-chaining)
- [Nullish coalescing](https://v8.dev/features/nullish-coalescing)



### 7.9

[blog](https://v8.dev/blog/v8-release-79)

<hr>


### 7.8

[blog](https://v8.dev/blog/v8-release-78)


### 7.7

<a href="#v77">

[blog](https://v8.dev/blog/v8-release-77)

- [The Intl.NumberFormat API](https://v8.dev/features/intl-numberformat)


### 7.6

<a href="#v76">

[blog](https://v8.dev/blog/v8-release-76)

- [Promise.allSettled](https://v8.dev/features/promise-combinators)
- Intl.DateTimeFormat improvements
  - formatRange
  - formatRangeToParts
- Improved BigInt support
  - toLocaleString


### 7.5

<a href="#v75">

[blog](https://v8.dev/blog/v8-release-75)

- [Numeric separators](https://v8.dev/features/numeric-separators)


### 7.4

<a href="#v74">

[blog](https://v8.dev/blog/v8-release-74)

- [Public class fields](https://v8.dev/features/class-fields#public-class-fields)
- [Private class fields](https://v8.dev/features/class-fields#private-class-fields)
- [Public and private static properties](https://v8.dev/features/class-fields#public-and-private-static-properties)
- [Simpler sub-classing](https://v8.dev/features/class-fields#simpler-subclassing)


### 7.3

<a href="#v73">

[blog](https://v8.dev/blog/v8-release-73)

- [Object.fromEntries](https://v8.dev/features/object-fromentries)
- [String.prototype.matchAll](https://v8.dev/features/string-matchall)


### 7.2

<a href="#v72">

[blog](https://v8.dev/blog/v8-release-72)

- [Intl.ListFormat](https://v8.dev/features/intl-listformat)
- [Well-formed JSON.stringify](https://v8.dev/features/well-formed-json-stringify)
- [Module namespace exports](https://v8.dev/features/module-namespace-exports)


### 7.1

<a href="#v71">

[blog](https://v8.dev/blog/v8-release-71)

- [The Intl.RelativeTimeFormat API](https://v8.dev/features/intl-relativetimeformat)


## 7.0

<a href="#v70">

[blog](https://v8.dev/blog/v8-release-70)

- Symbol.prototype.description


### 6.9

<a href="#v69">

[blog](https://v8.dev/blog/v8-release-69)

- [Array.prototype.flat and Array.prototype.flatMap](https://v8.dev/features/array-flat-flatmap)

<hr>

### 6.8

<a href="#v68" >

[blog](https://v8.dev/blog/v8-release-68)


### 6.7

[blog](https://v8.dev/blog/v8-release-67)


### 6.6

<a href="#v66">

[blog](https://v8.dev/blog/v8-release-66)

- [Function.prototype.toString revision](https://v8.dev/features/function-tostring)
- [Optional catch binding](https://v8.dev/features/optional-catch-binding)
- [One-sided string trimming](https://v8.dev/features/string-trimming)
- [Array.prototype.values](https://tc39.es/ecma262/#sec-array.prototype.values)


### 6.5

[blog](https://v8.dev/blog/v8-release-65)


### 6.4

<a href="#v64">

[blog](https://v8.dev/blog/v8-release-64)

- RegExp
  - [named capture groups](https://developers.google.com/web/updates/2017/07/upcoming-regexp-features#named_captures)
  - [unicode property escapes](https://mathiasbynens.be/notes/es-unicode-property-escapes)
- [import.meta](https://github.com/tc39/proposal-import-meta)
- [Intl.NumberFormat.prototype.formatToParts()](https://github.com/tc39/proposal-intl-formatToParts)


### 6.3

<a href="#v63">

[blog](https://v8.dev/blog/v8-release-63)

- [dynamic module import via import()](https://v8.dev/features/dynamic-import)
- [Promise.prototype.finally()](https://v8.dev/features/promise-finally)
- [async iterators/generators](https://github.com/tc39/proposal-async-iteration)
- [Intl.PluralRules](https://v8.dev/features/intl-pluralrules)


### 6.2

<a href="#v62">

[blog](https://v8.dev/blog/v8-release-62)

- More regular expressions features
  - [dotAll mode](https://github.com/tc39/proposal-regexp-dotall-flag)
  - [look behind assertions](https://github.com/tc39/proposal-regexp-lookbehind)
- [Template literal revision](https://tc39.es/proposal-template-literal-revision/)
- Increased max string length


### 6.1

<a href="#v61">

[blog](https://v8.dev/blog/v8-release-61)

<hr>

## 6.0

<a href="#v60" >

[blog](https://v8.dev/blog/v8-release-60)

- [Object rest/spread properties](https://v8.dev/features/object-rest-spread)
- SharedArrayBuffers
