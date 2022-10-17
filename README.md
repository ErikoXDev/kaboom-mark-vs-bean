# Kaboom  Template

A pre-made template for quick-starting a kaboom project.

## Contents

### Actions
`pages.yml` publishes your website automatically on every push to Github Pages. Make sure your code is working /shrug

Make sure you set up Github Pages in the repository settings and set the branch to "gh-pages"!

### FILES
- index.js
  - The index.js file contains the webserver used to server the bundled javascript and html.
- public (folder)
  - This folder contains the sounds and sprites folder, where you can put your sounds and sprites. You can access the sprites and sounds with ``loadSprite("sprites/e.png`)
- src (folder)
  - Contains main.js, the javascript file which will get bundled. You can add more javascript files and have the main.js file import them.
- dist (folder)
  - Contains the bundled "dist.js" and the index.html file.


### NPM SCRIPTS
- `runServer` starts the index.js file.
- `testServer` starts the index.js file with nodemon (You can install nodemon with `npm i -g nodemon`)
- `buildJs` bundles and minifies your javascript file.
- `noMinifyJs` is the same as buildJs, but skips the minifying process.
- `buildJsOnce` is just like buildJs, but without watch-mode.

### SETUP
1. Use the template to create a new repository
2. Clone your new repository
3. Run `npm install` to install all the required packages
4. Edit dist/index.html or src/main.js
5. Run the `buildJs` npm script and then run `runServer` to start hosting.
Alternatively the repository will publish to github pages after a push.

*Additional info: The buildJs script is set to watch-mode. You only have to run it once and it will always bundle your javascript when you change something. It can also throw Javascript errors. If you want to only build once, run the buildJsOnce script.*
