# Learning-React-Portfolio
A basic portfolio to showcase what you have learned! 👨🏻‍🎓

### Note:

- Instructions are listed in white.
- `Commands are listed in yellow.`
- [Hyperlinks are listed in blue.](./README.md)

## Tools
- [ ] [GitHub](https://github.com/)
- [ ] [Gitpod.io](https://gitpod.io/)
- [ ] [gh cli](https://cli.github.com/)

#### Local development
- [ ] [Node.js & npm](https://nodejs.org/en/download)
- [ ] [git](https://github.com/git-guides/install-git)
- [ ] [VSCode](https://code.visualstudio.com/)

## Getting Started

### Creating Your Repository & Dev Environmnet
1) Create a new repository on Github.com
2) Navigate to [gitpod.io/#github.com/your-username/your-repo](gitpod.io/#github.com/efwoods/Learning-React-Portfolio)
3) Install gh
   1) `sudo apt install gh`
4) Authenticate with github
   1) `gh auth login`
   2) Follow the command prompts, selecting 1 each time.
   3) Navigate to: https://github.com/login/device
   4) Copy/Paste the URL code into the browser
   5) Return to gitpod & press enter
   6) You are now logged in to the gh cli!

## Create A New React Project
1) `npx create-react-app my-portfolio`

### Styling with Tailwindcss & HeroIcons

#### Install Tailwindcss
- [Tailwindcss Installation Reference](https://tailwindcss.com/docs/installation)

1) `npm install -D tailwindcss`
2) `npx tailwindcss init`
3) modify "tailwind.config.js" with   `content: ["./src/**/*.{html,js}"],`
4) Add Tailwind directives to [index.css](./my-portfolio/src/index.css)
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

5) Implement tailwind directly into your html.  
- Example: `<h1 class="text-3xl font-bold underline">`
- [Tailwindcss Reference](https://nerdcave.com/tailwind-cheat-sheet)
- [Tailwind CSS IntelliSense for VsCode](https://open-vsx.org/vscode/item?itemName=bradlc.vscode-tailwindcss)

#### Install HeroIcons
- [HeroIcons](https://heroicons.com/)
- [HeroIcons Installation Reference](https://github.com/tailwindlabs/heroicons)
1) `npm install @heroicons/react`
2) Select the JSX from any icon from [HeroIcons](https://heroicons.com/)
3)  Import the icon directly into your component
  - Example: `import { BeakerIcon } from '@heroicons/react/24/solid'`
4) Use the icon as a component in your component:
  - Example: `<BeakerIcon className="h-6 w-6 text-blue-500" />`

### Clean & Create New Components
1) `mkdir src/components`
2) `code src/components/About.js`
3) Add the following in [About.js](./my-portfolio/src/components/About.js):
```js
export default function About() {}
```
4) Import [About](./my-portfolio/src/components/About.js) into [App.js](./my-portfolio/src/App.js)

```
import logo from './logo.svg';
import './App.css';
import React from "react";
import About from "./components/About"

function App() {
  return (
    <main>
      <About />
    </main>
  );
}

export default App;
```