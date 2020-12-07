# Grunt Starter

## A quick `gruntfile.js` for new projects

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
npm init -y

npm i -D node-sass grunt-sass grunt-contrib-concat grunt-contrib-uglify grunt-autoprefixer grunt-contrib-watch grunt-contrib-connect
```

---

### `.gitignore`

```git
node_modules
tmp
.tmp
.npm-debug.log
.sass-cache
*.css.map
```

---

### Live Reload

Listens on `port: 8000` by default

---

### Edit Folders

```
components/
-- scripts/
    -- script.js
    -- your_scripts.js
-- scss/
    -- _your_partials.scss
    -- _main.scss
    -- styles.scss
```

### Compiled Folders

---

```
dist/
-- js/
    -- scripts.js
    -- scripts.min.js
    -- scripts.min.js.map
-- css/
    -- styles.css
    -- styles.map.css
```

Cheers!  
Angela :two_hearts:
