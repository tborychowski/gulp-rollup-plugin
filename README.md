gulp-rollup-plugin
==================

Borrowed from [gulp-better-rollup](https://github.com/MikeKovarik/gulp-better-rollup) and upgraded to an ES module and Gulp v4.

Disclaimer: This package works for me. If it doesn't work for you, feel free to fork it and make it work.

## Installation
```sh
npm i -D rollup gulp-rollup-plugin
```

## Usage
```js
import rollup from 'gulp-rollup-plugin';

export function js () {
    return src('./src/index.js', { sourcemaps: true })
        .pipe(rollup({
            plugins: [],
        }, {
            file: 'index.js',
            format: 'esm',
        }))
        .pipe(dest('dist', { sourcemaps: true }));
}
```
