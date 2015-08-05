#glup tasks overview

1. define
generate define.js to bootstrap app
```gulp.task('define', function(){
    gulp.src(['./src/define/*.js', './src/define/ext/DEFINE_MENU.js', './src/define/ext/*.js'])
        .pipe($.jshint(jshintOption))
        .pipe($.jshint.reporter('default'))
        .pipe($.concat('define.js'))
        .pipe($.header([head], { pkg : pkg } ))
        .pipe(gulp.dest('tmp/config'));
}); 
```