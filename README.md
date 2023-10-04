<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Mean

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Student's t][t-distribution] distribution [expected value][expected-value].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [expected value][expected-value] for a [Student's t][t-distribution] random variable is

<!-- <equation class="equation" label="eq:t_expectation" align="center" raw="\mathbb{E}\left[ X \right] = 0" alt="Expected value for a Student's t distribution."> -->

```math
\mathbb{E}\left[ X \right] = 0
```

<!-- <div class="equation" align="center" data-raw-text="\mathbb{E}\left[ X \right] = 0" data-equation="eq:t_expectation">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/t/mean/docs/img/equation_t_expectation.svg" alt="Expected value for a Student's t distribution.">
    <br>
</div> -->

<!-- </equation> -->

for degrees of freedom `v` greater than one. For `v <= 1`, the mean is not defined.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import mean from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-t-mean@v0.1.1-deno/mod.js';
```

#### mean( v )

Returns the [expected value][expected-value] of a [Student's t][t-distribution] distribution with degrees of freedom `v`.

```javascript
var y = mean( 9.0 );
// returns 0.0

y = mean( 1.5 );
// returns 0.0
```

If provided `v <= 1`, the function returns `NaN`.

```javascript
var y = mean( -1.0 );
// returns NaN

y = mean( 0.8 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@deno/mod.js';
import round from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-round@deno/mod.js';
import mean from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-t-mean@v0.1.1-deno/mod.js';

var v;
var y;
var i;

for ( i = 0; i < 10; i++ ) {
    v = randu() * 20.0;
    y = mean( v );
    console.log( 'v: %d, E(X,v): %d', v.toFixed( 4 ), y.toFixed( 4 ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-t-mean.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-t-mean

[test-image]: https://github.com/stdlib-js/stats-base-dists-t-mean/actions/workflows/test.yml/badge.svg?branch=v0.1.1
[test-url]: https://github.com/stdlib-js/stats-base-dists-t-mean/actions/workflows/test.yml?query=branch:v0.1.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-t-mean/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-t-mean?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-t-mean.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-t-mean/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-t-mean/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-t-mean/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-t-mean/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-t-mean/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-t-mean/main/LICENSE

[t-distribution]: https://en.wikipedia.org/wiki/Student%27s_t-distribution

[expected-value]: https://en.wikipedia.org/wiki/Expected_value

</section>

<!-- /.links -->
