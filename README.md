# yoman-grunt-bower-
###安装
* 安装[yoman](http://yeoman.io/) `npm install -g yo`
* 安装[grunt](http://www.gruntjs.net/) `npm install -g grunt-cli`
* 安装[bower](http://bower.io/) `npm install -g bower`

###yoman 的使用
* yoman的generator异常强大，有“八字胡”的是官方出品
* 安装需要的generator `npm install -g generator-angular`
* 创建项目 `yo angular xxx`
* 按照提示选择需要的项，使用空格选择和取消选择

###grunt的使用
```
'use strict';

module.exports = function (grunt) {
  // Time how long tasks take. Can help when optimizing build times
  require('time-grunt')(grunt);

  // Automatically load required grunt tasks
  require('jit-grunt')(grunt, {
    useminPrepare: 'grunt-usemin'
  });

  // Configurable paths
  var config = {
    app: 'app',
    dist: 'dist'
  };
}
```
*
* grunt.initConfig({})配置task
```
 grunt.initConfig({
     // Empties folders to start fresh
    clean: {
      dist: {
        files: [{
          dot: true,
          src: [
            '.tmp',
            '<%= config.dist %>/*',
            '!<%= config.dist %>/.git*'
          ]
        }]
      },
      server: '.tmp'
    },
 })
```
