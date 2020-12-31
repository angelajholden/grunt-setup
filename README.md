# Grunt Starter :cherry_blossom:

## A quick `gruntfile.js` for new projects

### Dependencies

-   grunt
-   grunt-cli

### Dev Dependencies

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

### Or Start from Scratch

```bash
npm init -y

npm i grunt grunt-cli

npm i -D node-sass grunt-sass grunt-contrib-concat gruntjs/grunt-contrib-uglify#harmony grunt-autoprefixer grunt-contrib-watch grunt-contrib-connect
```

---

### `.gitignore`

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

Listens on `port: 8000` by default

---

### Edit Folders

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
