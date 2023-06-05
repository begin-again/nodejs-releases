Describe which new features have been added by version.

ESNext refers to the next upcoming version.

See [kangax](http://kangax.github.io/compat-table/es6/), [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) and [CanIUse.com](https://caniuse.com/ ) for browser support.

- [sources](#sources)
- [5](#5)
- [2015](#2015)
- [2016](#2016)
- [2017](#2017)
- [2018](#2018)
- [2019](#2019)
- [2020](#2020)
- [2021](#2021)
- [2022](#2022)
- [2023](#2023)
- [next](#next)

## sources

- [node green](https://node.green/)
- ponyFoo
  - [es6](https://ponyfoo.com/articles/es6)
  - [es2016](https://ponyfoo.com/articles/es2016-features-and-ecmascript-as-a-living-standard)
- Medium
  - [es2016 features](https://medium.com/better-programming/javascript-es2016-features-with-examples-a41b7aead589)
  - [es2017 features](https://medium.com/better-programming/javascript-es2017-features-with-examples-877f8406e770)
  - [es2018 features](https://medium.com/better-programming/javascript-es2018-features-with-examples-30fda8ac50fa)
  - [es2019 features](https://medium.com/better-programming/twelve-es10-features-in-twelve-simple-examples-6e8cc109f3d3)
  - [es2020 features](https://medium.com/better-programming/javascript-es2020-features-with-simple-examples-d301dbef2c37)
- GreyCampus
  - [JS versions](https://www.greycampus.com/blog/programming/java-script-versions)
- FreeCodeCamp
  - [es2020](https://www.freecodecamp.org/news/javascript-new-features-es2020/)

## 5

2009

- "use strict"
- [String.trim()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/trim)
- Array
  - Array.isArray()
  - Array.forEach()
  - Array.map()
  - Array.filter()
  - Array.reduce()
  - Array.reduceRight()
  - Array.every()
  - Array.some()
  - Array.indexOf()
  - Array.lastIndexOf()
- JSON
  - JSON.parse()
  - JSON.stringify()
- Date
  - Date.now()
  - date.valueOf()
- Property Getters and Setters
- New Object Property Methods
  - Object.defineProperty()

__Syntax__

- Property access `[ ]` on strings
- Trailing commas in array and object literals
- Multi-line string literals
- Reserved words as property names


## 2015

Also known as ES6. No IE11 support except through polyfills. [language spec](https://262.ecma-international.org/6.0/)

- [Destructuring Assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
- [Spread Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)
- [Rest Parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)
- [Default parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters)
- [Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
- [Template Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
- Object Literals
  - [property value short-hand](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#new_notations_in_ecmascript_2015) {foo: foo} same as {foo}
  - [Computed property names](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#computed_property_names), { [prefix + 'Foo']: 'bar' }, where prefix: 'moz', yields { mozFoo: 'bar' }
  - [Method definitions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#method_definitions) in an object literal can be declared using an alternative, more terse syntax, { foo () {} }
- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
  - Not “traditional” classes, syntax sugar on top of prototypal inheritance
- [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) and [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
- [Symbols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)
  - A new primitive type in ES6
- [Iterators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators#iterators)
  - define how to iterate over any object, not just arrays and array-likes
- [Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)
  - a special kind of iterator that can be declared using the function* generator () {} syntax
- [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
- [Maps](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
- [WeakMaps](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)
- [Sets](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
- [WeakSets](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)
- [Proxies](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy)
- [Reflection](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Reflect)
  - Full reflection API exposing the runtime-level meta-operations on objects. This is effectively the inverse of the Proxy API, and allows making calls corresponding to the same meta-operations as the proxy traps. Especially useful for implementing proxies.
- [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
  - Number.isNaN and Number.isFinite are like their global namesakes, except that they don’t coerce input to Number
  - Number.parseInt and Number.parseFloat are exactly the same as their global namesakes
  - Number.isInteger checks if input is a Number value that doesn’t have a decimal part
  - Number.EPSILON helps figure out negligible differences between two numbers – e.g. 0.1 + 0.2 and 0.3
  - Number.MAX_SAFE_INTEGER is the largest integer that can be safely and precisely represented in JavaScript
  - Number.MIN_SAFE_INTEGER is the smallest integer that can be safely and precisely represented in JavaScript
  - Number.isSafeInteger checks whether an integer is within those bounds, able to be represented safely and precisely
- Math
  - Math.sign – sign function of a number
  - Math.trunc – integer part of a number
  - Math.cbrt – cubic root of value, or ∛‾value
  - Math.expm1 – e to the value minus 1, or evalue - 1
  - Math.log1p – natural logarithm of value + 1, or ln(value + 1)
  - Math.log10 – base 10 logarithm of value, or log10(value)
  - Math.log2 – base 2 logarithm of value, or log2(value)
  - Math.sinh – hyperbolic sine of a number
  - Math.cosh – hyperbolic cosine of a number
  - Math.tanh – hyperbolic tangent of a number
  - Math.asinh – hyperbolic arc-sine of a number
  - Math.acosh – hyperbolic arc-cosine of a number
  - Math.atanh – hyperbolic arc-tangent of a number
  - Math.hypot – square root of the sum of squares
  - Math.clz32 – leading zero bits in the 32-bit representation of a number
  - Math.imul – C-like 32-bit multiplication
  - Math.fround – nearest single-precision float representation of a number
- Array
  - Array.from – create Array instances from array-like objects like arguments or iterables
  - Array.of – similar to new Array(...items), but without special cases
  - Array.prototype.copyWithin – copies a sequence of array elements into somewhere else in the array
  - Array.prototype.fill – fills all elements of an existing array with the provided value
  - Array.prototype.find – returns the first item to satisfy a callback
  - Array.prototype.findIndex – returns the index of the first item to satisfy a callback
  - Array.prototype.keys – returns an iterator that yields a sequence holding the keys for the array
  - Array.prototype.values – returns an iterator that yields a sequence holding the values for the array
  - Array.prototype.entries – returns an iterator that yields a sequence holding key value pairs for the array
  - Array.prototype[Symbol.iterator] – exactly the same as the Array.prototype.values method
- Object
  - Object.assign – recursive shallow overwrite for properties from target, ...objects
  - Object.is – like using the === operator programmatically, except it’s true for NaN vs NaN and false for +0 vs -0
  - Object.getOwnPropertySymbols – returns all own property symbols found on an object
  - Object.setPrototypeOf – changes prototype. Equivalent to Object.prototype.`__proto__` setter
- Strings & Unicode
  - String.prototype.startsWith – whether the string starts with value
  - String.prototype.endsWith – whether the string ends in value
  - String.prototype.includes – whether the string contains value anywhere
  - String.prototype.repeat – returns the string repeated amount times
  - String.prototype[Symbol.iterator] – lets you iterate over a sequence of unicode code points (not characters)
  - String.prototype.codePointAt – base-10 numeric representation of a code point at a given position in string
  - String.fromCodePoint – given ...codepoints, returns a string made of their unicode representations
  - String.prototype.normalize – returns a normalized version of the string’s unicode representation
- Modules
  - Strict Mode is turned on by default in the ES6 module system
  - ES6 modules are files that export an API
  - export default value exports a default binding
  - export var foo = 'bar' exports a named binding
  - Named exports are bindings that can be changed at any time from the module that’s exporting them
  - export { foo, bar } exports a list of named exports
  - export { foo as ponyfoo } aliases the export to be referenced as ponyfoo instead
  - export { foo as default } marks the named export as the default export
  - As a best practice, export default api at the end of all your modules, where api is an object, avoids confusion
  - Module loading is implementation-specific, allows inter-operation with CommonJS
  - import 'foo' loads the foo module into the current module
  - import foo from 'ponyfoo' assigns the default export of ponyfoo to a local foo variable
  - import {foo, bar} from 'baz' imports named exports foo and bar from the baz module
  - import {foo as bar} from 'baz' imports named export foo but aliased as a bar variable
  - import {default} from 'foo' also imports the default export
  - import {default as bar} from 'foo' imports the default export aliased as bar
  - import foo, {bar, baz} from 'foo' mixes default foo with named exports bar and baz in one declaration
  - import * as foo from 'foo' imports the namespace object
    - Contains all named exports in foo[name]
    - Contains the default export in foo.default, if a default export was declared in the module
- For..of
- For..in
- RegExp u mode
- Sub-classable Built-ins
  - built-ins like Array, Date and DOM Elements can be sub-classed
- Binary and Octal Literals
  - `0b111110111 === 503 // true`
  - `0o767 === 503 // true`
- Tail Calls
  - Calls in tail-position are guaranteed to not grow the stack unboundedly. Makes recursive algorithms safe in the face of unbounded inputs
- HTML-style comments

## 2016

[language spec](https://262.ecma-international.org/7.0/)
<br>
- [exponentiation (**) operator](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-exp-operator)
- [Array.prototype.includes](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-array.prototype.includes)
- [generator functions can't be used with "new"](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-createdynamicfunction)
- [generator throw() caught by inner generator](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-generatorfunction-objects)
- [strict fn w/ non-strict non-simple params is error](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-functiondeclarationinstantiation)
- [nested rest destructuring, declarations](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-destructuring-assignment)
- [nested rest destructuring, parameters](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-destructuring-assignment)
- [Proxy, "enumerate" handler removed](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-proxy-objects)
- [Proxy internal calls, Array.prototype.includes](http://www.ecma-international.org/ecma-262/7.0/index.html#sec-array.prototype.includes)


## 2017

[language spec](https://262.ecma-international.org/8.0/)
<br>
- [Object static methods](https://tc39.github.io/ecma262/#sec-properties-of-the-object-constructor)
- [String padding](https://github.com/tc39/proposal-string-pad-start-end)
- [trailing commas in function syntax](https://github.com/tc39/proposal-trailing-function-commas)
- [async functions](https://tc39.github.io/ecma262/#sec-async-function-definitions)
- [shared memory and atomics]()
  - Atomics.wake
- [RegExp "u" flag, case folding](https://github.com/tc39/ecma262/pull/525)
- [arguments.caller removed](https://github.com/tc39/ecma262/pull/689)
- [Object.prototype getter/setter methods](https://tc39.github.io/ecma262/#sec-object.prototype.__defineGetter__)
- [Proxy internal calls, getter/setter methods](https://tc39.github.io/ecma262/#sec-object.prototype.__defineGetter__)
- [assignments allowed in for-in head in non-strict mode](https://tc39.github.io/ecma262/#sec-initializers-in-forin-statement-heads)


## 2018

[language spec](https://262.ecma-international.org/9.0/)
<br>
- [object rest/spread properties](https://github.com/tc39/proposal-object-rest-spread)
- [Promise.prototype.finally](https://github.com/tc39/proposal-promise-finally)
- [s (dotAll) flag for regular expressions](https://tc39.github.io/ecma262/#sec-get-regexp.prototype.dotAll)
- [RegExp named capture groups](https://github.com/tc39/proposal-regexp-named-groups)
- [RegExp Lookbehind Assertions](https://github.com/tc39/proposal-regexp-lookbehind)
- [RegExp Unicode Property Escapes](https://github.com/tc39/proposal-regexp-unicode-property-escapes)
- [Asynchronous Iterators](https://github.com/tc39/proposal-async-iteration)
- [Proxy "ownKeys" handler, duplicate keys for non-extensible targets](https://tc39.es/ecma262/#sec-proxy-object-internal-methods-and-internal-slots-ownpropertykeys)
- [template literal revision](https://github.com/tc39/proposal-template-literal-revision)


## 2019

[language spec](https://262.ecma-international.org/10.0/)
<br>
- [Object.fromEntries](https://github.com/tc39/proposal-object-from-entries)
- [string trimming](https://github.com/tc39/proposal-string-left-right-trim)
- [Array.prototype.{flat, flatMap}](https://tc39.github.io/proposal-flatMap/)
  - Array.prototype.flat
  - Array.prototype.flatMap
- [optional catch binding](https://github.com/tc39/proposal-optional-catch-binding)
- [Symbol.prototype.description](https://github.com/tc39/Function-prototype-toString-revision)
- [JSON superset](https://github.com/tc39/proposal-json-superset)
- [Well-formed JSON.stringify](https://github.com/tc39/proposal-well-formed-stringify)


## 2020

[language spec](https://262.ecma-international.org/11.0/)
<br>
- [String.prototype.matchAll](https://github.com/tc39/String.prototype.matchAll)
  - throws on non-global regex
- [BigInt](https://github.com/tc39/proposal-bigint)
- [Promise.allSettled](https://github.com/tc39/proposal-promise-allSettled)
- [Nullish Coalescing operator](https://github.com/tc39/proposal-nullish-coalescing)
- [Optional Chaining operator](https://github.com/tc39/proposal-optional-chaining)
  - spread parameters after optional chaining
- [globalThis](https://github.com/tc39/proposal-global)


## 2021

[language spec](https://262.ecma-international.org/12.0/)
<br>
- [String.prototype.replaceAll](https://github.com/tc39/proposal-string-replace-all)
- [numeric separators](https://github.com/tc39/proposal-numeric-separator)
- [Promise.any](https://github.com/tc39/proposal-promise-any)
  - fulfillment
  - AggregateError
- [WeakReferences](https://github.com/tc39/proposal-weakrefs)
  - WeakRef minimal support
  - FinalizationRegistry minimal support
- [Logical Assignment](https://github.com/tc39/proposal-logical-assignment)
  - ||= basic support
  - ||= short-circuiting behavior
  - ||= setter not un-necessarily invoked
  - &&= basic support
  - &&= short-circuiting behavior
  - &&= setter not un-necessarily invoked
  - ??= basic support
  - ??= short-circuiting behavior
  - ??= setter not un-necessarily invoked


## 2022

[language spec](https://262.ecma-international.org/13.0/)
<br>

- [top-level await](https://github.com/tc39/proposal-top-level-await)
- [Ergonomic brand checks for private fields](https://github.com/tc39/proposal-private-fields-in-in)
- [at() method on the built-in index-ables](https://github.com/tc39/proposal-relative-indexing-method)
  - Array.prototype.at()
  - String.prototype.at()
  - %TypedArray%.prototype.at()
- [Class static initialization blocks](https://github.com/tc39/proposal-class-static-block)
- [Error Cause](https://github.com/tc39/proposal-error-cause)
- [Object.hasOwn()](https://github.com/tc39/proposal-accessible-object-hasownproperty)
- [Regex Match Indices](https://github.com/tc39/proposal-regexp-match-indices)
- [static class fields](https://github.com/tc39/proposal-static-class-features)
- [private class methods](https://github.com/tc39/proposal-private-methods)
- [class fields](https://github.com/tc39/proposal-class-fields)


## 2023

<br>

- [Array find from last](https://github.com/tc39/proposal-array-find-from-last)
- [Hash bang Grammar](https://github.com/tc39/proposal-hashbang/)
- [Symbols as weak map keys](https://github.com/tc39/proposal-symbols-as-weakmap-keys)
- [Change array by copy](https://github.com/tc39/proposal-change-array-by-copy)


## next

- [Legacy RegExp features in JavaScript](https://github.com/tc39/proposal-regexp-legacy-features)
