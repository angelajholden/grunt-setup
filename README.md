# Grunt Setup :cherry_blossom:

## A quick `gruntfile.js` for new projects

### Dependencies

-   grunt
-   grunt-cli

### Dev Dependencies

-   diff
-   node-sass
-   grunt-sass
-   grunt-contrib-concat
-   gruntjs/grunt-contrib-uglify#harmony
-   grunt-autoprefixer
-   grunt-contrib-watch
-   grunt-contrib-connect

---

### To Do

-   Find new Uglify package for JS
-   Check all packages for updates

---

### Use this Repo

```bash
git clone git@github.com:angelajholden/grunt-setup.git

npm update
```

### Start from Scratch

```bash
npm init -y

npm i grunt grunt-cli

npm i -D diff node-sass grunt-sass grunt-contrib-concat gruntjs/grunt-contrib-uglify#harmony grunt-autoprefixer grunt-contrib-watch grunt-contrib-connect
```

### On your marks, get set... GO!

In the terminal type `grunt` to start watching your files. The output should look something like this.

![Grunt running in the terminal](/grunt-in-terminal.png)

---

### `.gitignore`

Remember to add a `.gitignore` file before you `git init` your project.

```git
.DS_Store
node_modules
tmp
.tmp
.npm-debug.log
*.sass-cache
*.css.map
*.min.js.map
```

---

### Live Reload

Listens on `port: 8000` by default. Double check the grunt terminal output to be sure.

```bash
http://127.0.0.1:8000
```

---

### Source Folders

Create directories and files to edit your SCSS and JavaScript using this structure.

```
components/
|__ scripts/
    |__ script.js
    |__ your_scripts.js

|__ scss/
    |__ _your_partials.scss
    |__ _main.scss
    |__ styles.scss
```

---

### Compiled Folders

Grunt will compile your SCSS and JavaScript like this.

```
dist/
|__ js/
    |__ scripts.js
    |__ scripts.min.js
    |__ scripts.min.js.map

|__ css/
    |__ styles.css
    |__ styles.map.css
```

Cheers!  
Angela :two_hearts:
