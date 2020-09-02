# 🚨 THIS IS A FORK OF PRETTIER 🚨

This is a fork of Prettier which formats HTML (or similar) using the single-attribute-per-line style, when
there are 2 or more attributes. The official Prettier will follow this same approach, but only once the
line length reaches the maximum.

From this:
```html
<button id="actionDoSomething" class="btn" type="button" @click="action">
  <span class="btn-inner">Primary Action</span>
</button>
```

To this:
```html
<button
  id="actionDoSomething"
  class="btn"
  type="button"
  @click="action"
>
  <span class="btn-inner">Primary Action</span>
</button>
```

This fork simply adds 1 new line of code to Prettier's HTML printer. All HTML-like languages should
be supported. All Prettier options should function exactly the same as they do with the upstream Prettier.

## Installing

Use the following to install this package as an alias of Prettier. Anything which searches `node_modules`
for Prettier will use this fork instead.

```bash
npm install --save-dev prettier@npm:@rakacreative/prettier
```

**IMPORTANT:** npm's alias feature does not currently symlink package binaries into
`node_modules/.bin`. You can still execute this fork's CLI by directly accessing the
`bin-prettier.js` file, i.e. `node_modules/prettier/bin-prettier.js`.

## Credits
Credit for the required changes to achieve the desired attribute formatting goes to
[kankje](https://github.com/kankje) via
[this pull
request](https://github.com/prettier/prettier/pull/6644/commits/1e85e439cacea189db4516965a3088a3a94b0ac2#diff-8b490542076a1de9d16d350dd3f39420).

## Additional Resources

This package may no longer be necessary if any of the following are merged into the upstream
Prettier:
- https://github.com/prettier/prettier/issues/5919
- https://github.com/prettier/prettier/pull/6113
- https://github.com/prettier/prettier/pull/6644/commits/1e85e439cacea189db4516965a3088a3a94b0ac2

Additional discussion about the subject:
- https://github.com/prettier/prettier/issues/5501
- https://github.com/prettier/prettier/issues/3101


<hr>
<br>
<br>

![Prettier Banner](https://raw.githubusercontent.com/prettier/prettier-logo/master/images/prettier-banner-light.png)

<h2 align="center">Opinionated Code Formatter</h2>

<p align="center">
  <em>
    JavaScript
    · TypeScript
    · Flow
    · JSX
    · JSON
  </em>
  <br />
  <em>
    CSS
    · SCSS
    · Less
  </em>
  <br />
  <em>
    HTML
    · Vue
    · Angular
  </em>
  <br />
  <em>
    GraphQL
    · Markdown
    · YAML
  </em>
  <br />
  <em>
    <a href="https://prettier.io/docs/en/plugins.html">
      Your favorite language?
    </a>
  </em>
</p>

<p align="center">
  <a href="https://github.com/prettier/prettier/actions?query=workflow%3AProd+branch%3Amaster">
    <img alt="Github Actions Build Status" src="https://img.shields.io/github/workflow/status/prettier/prettier/Prod?label=Prod&style=flat-square"></a>
  <a href="https://github.com/prettier/prettier/actions?query=workflow%3ADev+branch%3Amaster">
    <img alt="Github Actions Build Status" src="https://img.shields.io/github/workflow/status/prettier/prettier/Dev?label=Dev&style=flat-square"></a>
  <a href="https://github.com/prettier/prettier/actions?query=workflow%3ALint+branch%3Amaster">
    <img alt="Github Actions Build Status" src="https://img.shields.io/github/workflow/status/prettier/prettier/Lint?label=Lint&style=flat-square"></a>
  <a href="https://codecov.io/gh/prettier/prettier">
    <img alt="Codecov Coverage Status" src="https://img.shields.io/codecov/c/github/prettier/prettier.svg?style=flat-square"></a>
  <a href="https://twitter.com/acdlite/status/974390255393505280">
    <img alt="Blazing Fast" src="https://img.shields.io/badge/speed-blazing%20%F0%9F%94%A5-brightgreen.svg?style=flat-square"></a>
  <br/>
  <a href="https://www.npmjs.com/package/prettier">
    <img alt="npm version" src="https://img.shields.io/npm/v/prettier.svg?style=flat-square"></a>
  <a href="https://www.npmjs.com/package/prettier">
    <img alt="weekly downloads from npm" src="https://img.shields.io/npm/dw/prettier.svg?style=flat-square"></a>
  <a href="#badge">
    <img alt="code style: prettier" src="https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square"></a>
  <a href="https://gitter.im/jlongster/prettier">
    <img alt="Chat on Gitter" src="https://img.shields.io/gitter/room/jlongster/prettier.svg?style=flat-square"></a>
  <a href="https://twitter.com/PrettierCode">
    <img alt="Follow Prettier on Twitter" src="https://img.shields.io/twitter/follow/prettiercode.svg?label=follow+prettier&style=flat-square"></a>
</p>

## Intro

Prettier is an opinionated code formatter. It enforces a consistent style by parsing your code and re-printing it with its own rules that take the maximum line length into account, wrapping code when necessary.

### Input

<!-- prettier-ignore -->
```js
foo(reallyLongArg(), omgSoManyParameters(), IShouldRefactorThis(), isThereSeriouslyAnotherOne());
```

### Output

```js
foo(
  reallyLongArg(),
  omgSoManyParameters(),
  IShouldRefactorThis(),
  isThereSeriouslyAnotherOne()
);
```

Prettier can be run [in your editor](http://prettier.io/docs/en/editors.html) on-save, in a [pre-commit hook](https://prettier.io/docs/en/precommit.html), or in [CI environments](https://prettier.io/docs/en/cli.html#list-different) to ensure your codebase has a consistent style without devs ever having to post a nit-picky comment on a code review ever again!

---

**[Documentation](https://prettier.io/docs/en/)**

<!-- prettier-ignore -->
[Install](https://prettier.io/docs/en/install.html) ·
[Options](https://prettier.io/docs/en/options.html) ·
[CLI](https://prettier.io/docs/en/cli.html) ·
[API](https://prettier.io/docs/en/api.html)

**[Playground](https://prettier.io/playground/)**

---

## Badge

Show the world you're using _Prettier_ → [![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)

```md
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
