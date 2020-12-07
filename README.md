# Grunt Starter

## A quick starter for new projects

### Dependencies

-   node-sass
-   grunt-sass
-   grunt-contrib-concat
-   grunt-contrib-uglify
-   grunt-autoprefixer
-   grunt-contrib-watch
-   grunt-contrib-connect

---

### Getting Started

```bash
npm install
```

### Edit Folders

-   `components/`
    -- `scripts/`
    ---- `script.js`
    ---- `your_scripts.js`
    --`scss/`
    ---- `_your_partials.scss`
    ---- `_main.scss`
    ---- `styles.scss`

### Compiled Folders

-   `dist/`
    -- `js/`
    ---- `scripts.js`
    ---- `scripts.min.js`
    ---- `scripts.min.js.map`
    --`css/`
    ---- `styles.css`
    ---- `styles.map.css`

---

```js
module.exports = function (grunt) {
    const sass = require("node-sass");
    grunt.initConfig({
        concat: {
            options: {
                //options go here
            },
            dist: {
                src: ["components/scripts/*.js"],
                dest: "dist/js/scripts.js",
            },
        }, //concat js

        uglify: {
            options: {
                sourceMap: true,
            },
            dist: {
                files: [
                    {
                        src: "dist/js/scripts.js",
                        dest: "dist/js/scripts.min.js",
                    },
                ],
            },
        }, //uglify js

        sass: {
            options: {
                implementation: sass,
                sourceMap: true,
                outputStyle: "compressed",
            },
            dist: {
                files: [
                    {
                        src: "components/scss/styles.scss",
                        dest: "dist/css/styles.min.css",
                    },
                ],
            },
        }, //sass

        autoprefixer: {
            options: {
                browsers: ["last 4 versions"],
                map: true,
            },
            files: {
                src: "dist/css/*.css",
                dest: "",
            },
        }, //autoprefixer

        connect: {
            server: {
                options: {
                    hostname: "127.0.0.1",
                    port: "8000",
                    useAvailablePort: true,
                    base: "./",
                    livereload: true,
                },
            },
        }, //livereload

        watch: {
            options: {
                spawn: false,
                livereload: true,
            },
            scripts: {
                files: [
                    "dist/",
                    "components/js/*.js",
                    "components/scss/*.scss",
                ],
                tasks: ["concat", "uglify", "sass", "autoprefixer", "connect"],
            },
        }, //watch
    }); //initConfig

    grunt.loadNpmTasks("grunt-contrib-concat");
    grunt.loadNpmTasks("grunt-contrib-uglify");
    grunt.loadNpmTasks("grunt-sass");
    grunt.loadNpmTasks("grunt-autoprefixer");
    grunt.loadNpmTasks("grunt-contrib-watch");
    grunt.loadNpmTasks("grunt-contrib-connect");
    grunt.registerTask("default", [
        "concat",
        "uglify",
        "sass",
        "autoprefixer",
        "connect",
        "watch",
    ]);
}; //wrapper function
```
