# Tailwind_CLI_installation

**step 1:**
we have to chack is NPM inistalled in our Computer/Machine or not?
So we can chack NPM virson by this `node -v` command and it should be higher then `Node.js>=12.3.0`.

**step 1:**
We have to initialise a NODE Project with this `npm init -y` command.


**step 1:**
Then we have to initialise taildwindcss as Developer Dependentis in our Project with this `npm i -D tailwindcss` command.

**step 1:**
we have to insatll Tailwind CSS Intellisense Plugin in our VS Code for smuth working exparience.

**Install Tailwind CSS**
we have to install tailwindcss via npm, and create your tailwind.config.js file.
```
npm install -D tailwindcss
```
then
```
npx tailwindcss init
```
**Configure our template paths**
we have to add the paths to all of our template files in `tailwind.config.js` file.
```
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
**Add the Tailwind directives to our CSS**

We have to add the @tailwind directives for each of Tailwind’s layers to our `src/input.css` main CSS file.
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
**Create Folder/Files**
In this Project we need `src` Folder and in this folder we have to create two files `index.html` and `tailwind.css` it could be any Name, Dosen't mater.

**Create Script**
we have to add script in our `package.json` file.
```
"scripts": {
    "build":"npx tailwindcss -i ./src/tailwind.css -o ./dist/style.css --watch"
  },
  ```

**Start the Tailwind CLI build process**
Now we can start our Tailwind CLI build by this Command: 
```
npm run build
```

**VS Code Error sign Problem**
In this position we may face a problem? VS Code show error sign in our css code.
VS Code can not ditecting TaildwindCSS that's the reson.

**Solve VS Code Problems**
We have to create a `.vscode` Folder then create a `settings.json` File.

we have to add some lines of code in this `settings.json` file.
```
{
    "css.validate": false,
    "tailwindCSS.emmetCompletions": true
}
```

**Start using Tailwind in your HTML**
we have to add our compiled CSS file to the <head> in `src/index.html` File and it's time to start using Tailwind’s utility classes to style our content

```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
 ```
  
