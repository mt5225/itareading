#glup tasks overview, from ./gulp/server.js

#overall steps

```
var taskArr = ['livereload', 'sass', 'define', 'Timeline', 'Toolbar', 'contextMenuLibs', 'utils', 'inject', 'watch'];
```
**global vars registered as header and footer** (timeline.js for example)

```
var globalItems = [
	'Timeline'
];

var predef = [
    'graph'
];


var head = [
        banner,
        gap.getGlobal(globalItems),
        '(function(graph){',
        "'use strict';",
        ''
    ].join('\n\n\n'),

    foot = [
        '',
        'graph.Timeline = Timeline;',
        '})(nameSpace.reg(\'graph\'));'
    ].join('\n\n\n');
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
register **timeline** as **graph.Timeline**
```
gulp.src(['./src/Timeline/__init__.js', './src/Timeline/**/*.js'])
```

## step 4. Toolbar.js
register **toolbar** as **graph.Toolbar**
```
 gulp.src(['./src/Toolbar/__init__.js', './src/Toolbar/*.js','./src/Toolbar/lib/**/*.js'])
```

## step 5. contextMenuLibs.js

```
var globalItems = [
    'mxImage', 'mxClipboard', 'saveAs', 'mxHierarchicalLayout', 'mxConstants', 'mxCircleLayout', 'mxFastOrganicLayout',
    'mxParallelEdgeLayout', 'mxStackLayout'
];
```
