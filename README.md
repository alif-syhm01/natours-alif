
# Hi 👋, I'm Alif

For this project, I make them with SASS or we can said CSS Preprocessor. This project is the result of my learning journey in SASS. Teaching by Jonas Schmedtmann on one his course in udemy.

If you wanna see the result, don't forget to follow this procedure to make this project is running on your device.


## Initialitation of node package manager

```javascript
npm init
```
In this step you will have some a question to make the package.json then you will use for this project (build the css from sass), just following the simple question.

## Installing node package module

```javascript
npm install
```
After you finish, then you running that command to installing `node_modules`.

## Installing depedencies

```javascript
- npm install autoprefixer --save-dev
- npm install concat --save-dev
- npm install node-sass --save-dev
- npm install npm-run-all --save-dev
- npm install postcss-cli --save-dev
```
After that you must install some optional depedencies to support the package who help to build the sass into css code.

## Custom the scripts

```javascript
"scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },
```
After you install all that you need, then you must copy all that `"scripts"` into your `package.json`

## First build

```javascript
npm run build:css
```
The first thing that you need to run is build the css, because everything the folder and file is already structured, you just need to build the css **(if you want to dive into this project just feel free, and you must know what you do in this project ✌️)**

## Running on your device 😄

```javascript
npm start
```
If you feel completed the step, finally you can run the project using that command in your device! 😎
