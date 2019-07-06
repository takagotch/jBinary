### jBinary
---
https://github.com/jDataView/jBinary

```js
require.config({
  paths: {
    jdataview: '//jdataview.github.io/dist/jdataview',
    jbinary: '//jdataview.github.io/dist/jbinary',
    TAR: '//jdataview.github.io/jBinary.Repo/typeSets/tar'
  }
});
require(['jbinary', 'TAR'], function(jBinary, TAR){
  jBinary.load('sample.tar', TAR).then(function(jb/* : jBinary */){
    bar files = jb.readAll();
    files.forEach(function(file){
      file.name = file.name.toUpperCase();
    });
    jb.writeAll(files, 0);
    jb.saveAs('sample.new.tar');
  });
});
```

```js
// Gruntfile.js
module.exports = function (grunt) {
  require('load-grunt-config')(grunt, {
    data: {
      pkgName: 'jbinary'
    }
  });
};
```

```
```
