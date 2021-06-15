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

# Spam Assassin

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> The [Spam Assassin][spam-assassin] public mail corpus.

<section class="intro">

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/datasets-spam-assassin
```

</section>

<section class="usage">

## Usage

```javascript
var corpus = require( '@stdlib/datasets-spam-assassin' );
```

#### corpus()

Returns the [Spam Assassin][spam-assassin] public mail corpus.

```javascript
var data = corpus();
// returns [{...},{...},...]
```

Each `array` element has the following fields:

-   `id`: message id (relative to message `group`)
-   `group`: message group
-   `checksum`: object containing checksum info
-   `text`: message text (including headers)

The message `group` may be one of the following:

-   `easy-ham-1`: easier to detect non-spam e-mails (2500 messages)
-   `easy-ham-2`: easier to detect non-spam e-mails collected at a later date (1400 messages)
-   `hard-ham-1`: harder to detect non-spam e-mails (250 messages)
-   `spam-1`: spam e-mails (500 messages)
-   `spam-2`: spam e-mails collected at a later date (1396 messages)

The `checksum` object contains the following fields:

-   `type`: checksum type (e.g., MD5)
-   `value`: checksum value

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better example. Possibly a spam classifier. -->

<!-- eslint no-undef: "error" -->

```javascript
var corpus = require( '@stdlib/datasets-spam-assassin' );

var data;
var i;

data = corpus();
for ( i = 0; i < data.length; i++ ) {
    console.log( 'Character Count: %d', data[ i ].text.length );
}
```

</section>

<!-- /.examples -->

* * *

<section class="cli">

## CLI

<section class="installation">

## Installation

To use the module as a general utility, install the module globally

```bash
npm install -g @stdlib/datasets-spam-assassin
```

</section>

<section class="usage">

### Usage

```text
Usage: spam-assassin [options]

Options:

  -h,    --help                Print this message.
  -V,    --version             Print the package version.
         --format fmt          Output format: 'txt' or 'ndjson'.
```

</section>

<!-- /.usage -->

<section class="notes">

### Notes

-   The CLI supports two output formats: plain text (`txt`) and newline-delimited JSON ([NDJSON][ndjson]). The default output format is `txt`.

</section>

<!-- /.notes -->

<section class="examples">

### Examples

```bash
$ spam-assassin
```

</section>

<!-- /.examples -->

</section>

<!-- /.cli -->

<!-- <license> -->

* * *

## License

The data files (databases) are licensed under an [Open Data Commons Public Domain Dedication & License 1.0][pddl-1.0] and their contents are licensed under [Creative Commons Zero v1.0 Universal][cc0]. The software is licensed under [Apache License, Version 2.0][apache-license].

<!-- </license> -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/datasets-spam-assassin.svg
[npm-url]: https://npmjs.org/package/@stdlib/datasets-spam-assassin

[test-image]: https://github.com/stdlib-js/datasets-spam-assassin/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/datasets-spam-assassin/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/datasets-spam-assassin/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/datasets-spam-assassin?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/datasets-spam-assassin
[dependencies-url]: https://david-dm.org/stdlib-js/datasets-spam-assassin/main

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/datasets-spam-assassin/main/LICENSE

[pddl-1.0]: http://opendatacommons.org/licenses/pddl/1.0/

[cc0]: https://creativecommons.org/publicdomain/zero/1.0

[apache-license]: https://www.apache.org/licenses/LICENSE-2.0

[ndjson]: http://specs.frictionlessdata.io/ndjson/

[spam-assassin]: http://spamassassin.apache.org/old/publiccorpus/readme.html

</section>

<!-- /.links -->
