# AdminLTE Midnight Dark Theme
[AdminLTE](https://github.com/almasaeed2010/AdminLTE) uses `skins` to produce minor changes to its colour schema.

![alt text](https://github.com/anvyst/adminlte-skin-midnight/blob/master/examples/skin-midnight-overview.png?raw=true)

# Installation

For production system it's enough to copy `dist/css/skins/skin-midnight.min.css` files
to where your styles reside and include it to your page.

# Contribution

Current theme was developed using AdminLTE v2.3.8 release, thus some of the packages
might be outdated, like `grunt`.

For patching and contributing to Midnight theme skin, you should locally clone AdminLTE
repository:

```bash

git clone git@github.com:almasaeed2010/AdminLTE.git
cd AdminLTE
yarn
```

Add `skin-midnight` to `Gruntfile.js` build instructions:

```less

/* in build/less/skins/_all_skins.less add following line*/
@import "skin-midnight.less";

```

```javascript

// in Grunfile.js add following lines:

grunt.initConfig({
  less: {
    ...
    development: {
      files: {
        ...
        "dist/css/skins/skin-midnight.css": "build/less/skins/skin-midnight.less",
      }
    }
  },
  production: {
    ...
    files: {
      ...
      "dist/css/skins/skin-midnight.min.css": "build/less/skins/skin-midnight.less",
    }
  }
});
```

Once it's all done you can run `grunt less` or `grunt watch` to make sure that `skin-midnight` was properly compiled.

**Note:** v2.3.8 AdminLTE uses v0.4.5 of `grunt` so you might have to run `npm i -g grunt@0.4.5` 

# References

* AdminLTE [repository](https://github.com/almasaeed2010/AdminLTE)
* AdminLTE [demo](https://adminlte.io/themes/AdminLTE/index2.html)
