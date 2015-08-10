#glup tasks overview, from ./gulp/server.js

#overall steps

```
var taskArr = ['livereload', 'sass', 'define', 'Timeline', 'Toolbar', 'contextMenuLibs', 'utils', 'inject', 'watch'];
```

## step 1. sass.js

```gulp.task('sass', function () {
	var srcPath = './src/scss/*.scss';}```

## step 2. define.js
generate define.js to bootstrap app
```
gulp.task('define', function(){
    gulp.src(['./src/define/*.js', './src/define/ext/DEFINE_MENU.js', './src/define/ext/*.js'])
        .pipe($.jshint(jshintOption))
        .pipe($.jshint.reporter('default'))
        .pipe($.concat('define.js'))
        .pipe($.header([head], { pkg : pkg } ))
        .pipe(gulp.dest('tmp/config'));
}); 
```

## step 3. Timeline.js