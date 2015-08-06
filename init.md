
# constants and nameplace
* Contants
```
(function(self){
self.con1 = ...
self.con2 = ...
})(window);
```
* Namespace
 1. an ```window.namespace``` object with add/remove/isDefined methond
 2. 3 main namespaces
 ```
self.nameSpace.reg('mmdb');
self.nameSpace.reg('graph');
self.nameSpace.reg('graph.CACHE_CI');
 ```

#bootstrap app
- app bootstap is wired by gulp
```
<!-- build:appJs js/app.js -->
<!-- inject:appJs -->
<!-- endinject -->
```
- ext config is definded in ```define.js```
```gulp.src(['./src/define/*.js', './src/define/ext/DEFINE_MENU.js', './src/define/ext/*.js'])```

- js inject by gulp
``` js/plugins.js  js/graph.js js/assets.js js/app.js
```

