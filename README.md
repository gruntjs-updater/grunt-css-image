# grunt-css-image

> Plugin to generate css file wto bind all images from folder

## Getting Started
This plugin requires Grunt `~0.4.2`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-css-image --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-css-image');
```

## The "css_image" task

### Overview
In your project's Gruntfile, add a section named `css_image` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  css_image: {
    dist:{
      files:[{
        cwd:"app/images/"
        src: "**/*.{png,jpg,gif,jpeg}"
        dest: "app/styles/_img.css"
      }]
      options:{
        prefix:"img_",
        images_path:"../images"
      }
    }
  },
});
```

### Options

#### options.prefix
Type: `String`
Default value: `'img_'`

Css prefix. For example: .img_sample_image for sample_image.png

#### options.images_path
Type: `String`
Default value: `'../images'`

Path to image source.

### Usage Examples

#### Default Options
In this example task search all images from "app/images/" according mask "**/*.{png,jpg,gif,jpeg}" and write css file in "app/styles/img.css"
with css prefix "_img" and path to image folder "../images"

```js
grunt.initConfig({
  css_image: {
    dist:{
      files:[{
        cwd:"app/images/"
        src: "**/*.{png,jpg,gif,jpeg}"
        dest: "app/styles/img.css"
      }]
      options:{
        prefix:"img_",
        images_path:"../images"
      }
    }
  },
});
```
#### Sample resulting css
```css
/* This file is generated */
.img_credits_footer{
  background: transparent url("../images/base/credits_footer.png") 0 0 no-repeat ;
  width: 376px;
  height: 94px;
  text-indent: -5000px;
  display: block;
  z-index: 0;
}
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
