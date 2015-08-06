##gulp task
inject graphic related javascript library ```gulp/inject.js```
```
var graphJs = [

	// GRAPH
    "plugins/mxGraph/mxClient.js",
    "plugins/mxGraph/Graph.js",
    "plugins/mxGraph/Graph_extend.js",
    "plugins/mxGraph/Editor.js",
    "plugins/mxGraph/Actions.js",
    "plugins/mxGraph/Shapes.js",
    "plugins/mxGraph/Sidebar.js",
    "plugins/mxGraph/sanitizer/sanitizer.min.js",

	// WEBGL
	'plugins/threejs/three.min.js',
	'plugins/threejs/lisu.js',
	'plugins/threejs/OrbitControls.js',
	'plugins/threejs/stats.min.js',
	'plugins/threejs/THREEx.ContainerResize.js',
	'plugins/threejs/threex.dynamictexture.js',
	'plugins/threejs/MTLLoader.js',
	'plugins/threejs/OBJLoader.js',
	'plugins/threejs/OBJMTLLoader.js'
];
```

