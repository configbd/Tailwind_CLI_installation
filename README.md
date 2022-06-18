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
npx tailwindcss init
```
**Configure our template paths**
we have to add the paths to all of your template files in our `tailwind.config.js` file.
```
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
**Add the Tailwind directives to your CSS**

We have to add the @tailwind directives for each of Tailwind’s layers to our `src/input.css` main CSS file.
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
**Create Script**
we have to add script in our `package.json` file.
```
"scripts": {
    "build":"npx tailwindcss -i ./src/tailwind.css -o ./dist/style.css --watch"
  },
  ```

**Start the Tailwind CLI build process**


