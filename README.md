# gulp-img64-html [![Build Status](https://travis-ci.org/247even/gulp-img64.png)](https://travis-ci.org/247even/gulp-img64)

Based in 247even's gulp-img64. Convert and replace image-files within your DOM/HTML to base64-encoded data.

### Gulp Task:

```js
var gulp = require('gulp');
var img64Html = require('gulp-img64-html');

gulp.task('default', function () {
	gulp.src('index.html')
	.pipe(img64Html())
	.pipe(gulp.dest('path'));
});
```

### index.html - Before:

```html
<img src="sample.png" />
```


### path/index.html - After:

```html
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAQAAAAEACAYAAABccqhmAACksUlEQVR42ux9B5glV3F195ud2dkkaSXxE22SDTYigwwWSUQHsAgCEyTAgBAgE0wGA79JwiKDAIlkhEgiRxF[and so on...]">
```

### Only option: `ignoreExternal`

Default: `false` - Boolean

```js
img64Html({
	ignoreExternal: true // will skip http & https
})
```

### License

MIT © 247even
