gulp-rollup-plugin
==================

Borrowed from [gulp-better-rollup](https://github.com/MikeKovarik/gulp-better-rollup) and upgraded to an ES module and Gulp v4.

Disclaimer: This package works for me. If it doesn't work for you, feel free to fork it and make it work.

## Installation
```sh
npm i -D rollup gulp-best-rollup
```

## Usage
```js
import sourcemaps from 'gulp-sourcemaps';
import rollup from 'gulp-best-rollup';

export function js () {
    return src('./src/index.js')
        .pipe(sourcemaps.init())
        .pipe(rollup({
            plugins: [],
        }, {
            file: 'index.js',
            format: 'esm',
        }))
        .pipe(sourcemaps.write(''))
        .pipe(dest('dist'));
}
```
