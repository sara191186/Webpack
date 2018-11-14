Install node and npm, if not check this blog https://blog.teamtreehouse.com/install-node-js-npm-windows

Open command prompt and switch to your working directory

Use `npm init -y` to create `package.json` and `package-lock.json` in the current directory

Type `npm install webpack webpack-cli -save-dev` to install webpack and webpack cli

Open `package.json` and you can able to see wepack and webpack-cli added as a development dependencies

```
"devDependencies": {
  "webpack": "^4.25.1",
  "webpack-cli": "^3.1.2"
}

```
Add the following lines under `"scripts"` in package.json

```
"scripts": {
 "build": "webpack --config webpack.config.js"
}

```
The above lines of code tells npm to run webpack using this config file

Create a new file `webpack.config.js` in the root directory and add the following lines of code to that file

```
module.exports = {
  entry: './main.js',
  output: {
    filename: './bundle.js'
  }
};

```
Next create `main.js` and `index.html` in the root folder

To run the project, type `npm run build`

What it does is, it runs the webpack using the config file and create `bundle.js` under the dist directory.
xcvxvxv
