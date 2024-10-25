# Where to find the React documentation?
The old react documentation was on another website, but the new and current documentation is on <a href="https://react.dev/" target="_blank">react.dev</a>

# Getting started
## Create a new project
### ```create-react-app```
Run the following command to create a core React app without any of the NEXT.js garbage:
```bash
npx create-react-app
```
But that is really slow, and by that I mean painfully slow. So don't do that.
There is however some hope for us, we don't usually use this nowadays, but its good to have knowledge about this.

### Vite
Vite is a bundler.

Run this command to create a vite app
```bash
npm create vite@latest
```
Then run
```bash
npm i
```
Then run
```bash
npm run dev
```

#### Removing unncessary files
<ul>
<li>

Delete ```src/assets``` we don't need it right now.
</li>
<li>

Delete ```src/App.css```. We will talk about CSS later.
</li>
<li>

Delete ```src/index.css```. We will do css later
</li>

### Removing unnecerry imports
<ul>
	<li>

Remove this statement from ```main.jsx```:
```jsx
import './index.css'
```
</li>
<li>

Remove these statements from ```App.jsx```:
```jsx
import { useState } from 'react'
import reactLogo from './assets/react.svg'
import viteLogo from '/vite.svg'
import './App.css'
```
Because we deleted ```assets``` and we don't have any CSS files nor we know how touse ```useState```
</li>
<li>

Remove this return value of ```App()``` in ```App.jsx```:

```jsx
<>
      <div>
        <a href="https://vite.dev" target="_blank">
          <img src={viteLogo} className="logo" alt="Vite logo" />
        </a>
        <a href="https://react.dev" target="_blank">
          <img src={reactLogo} className="logo react" alt="React logo" />
        </a>
      </div>
      <h1>Vite + React</h1>
      <div className="card">
        <button onClick={() => setCount((count) => count + 1)}>
          count is {count}
        </button>
        <p>
          Edit <code>src/App.jsx</code> and save to test HMR
        </p>
      </div>
      <p className="read-the-docs">
        Click on the Vite and React logos to learn more
      </p>
    </>
```
</li>
<li>

Remove this from ```App.jsx``` because we have no idea what it is:
```jsx
  const [count, setCount] = useState(0)
```
</li>
</ul>

### Writing ```jsx```
Put this in the return value of ```App()``` in ```App.jsx```:
```jsx
<h1>Put your text here</h1>
```