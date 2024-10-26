# ```create-react-app```
## Folders
### ```node_modules```
It contains all the dependencies listed in the ```package.json```.

If you have the ```package.json``` you can easily install it just by:
```bash
npm i
```
### ```src```
It contains our code files, that includes ```.js``` and ```.css``` files.


## Files
### ```.gitignore```
It contains the files **that we don't to push to GitHub**, that would be things like ```node_modules```, ```.env``` files etc..

### ```package-lock.json```
This has all the dependencies locked at a certain version that the project won't work without those exact versions of those dependencies.

# ```vite``` app
## Loading the main file
In ```create-react-app``` the ```index.js``` file is loaded by ```react-scripts``` so it goes and inserts the ```<script>``` tag in ```public/index.html``` at the time of compilation.

Vite inserts the ```<script>``` for the ```main.jsx``` directly in the ```index.html``` file in ```/``` directory.

## ```<React.StrictMode>```
It is also sometimes written ```<StrictMode>``` but you have to import it as follows:
```js
import { StrictMode } from 'react'
```
You can also just get rid of this ```<StrictMode>``` because it doesn't matter as much because its just for development optimization.

### So as you saw, there is not much difference in these two, its just that Vite is a bit more lightweight than ```create-react-app``` because it does not include any of the unnecery ```react-scripts```.

# New work
## Copying the project
I am going to use the same Vite project as the lesson before.
## Creating a new component
### Create a new file
Call it any thing you want with ```.js``` at the end.

The standard while creating components is ```.jsx``` but its ok for now as I am learning.

I'll call it ```coffee.js```.

And that is a problem, if we used ```create-react-app``` we could do that but if we use ```vite```, we can't do that.

So we will have to call it ```coffee.jsx```.

## Naming convention 
If just do:
```jsx
function coffee() {
	return(
		<h3>☕</h3>
		)
}

export default coffee
```
It will give an error

The name of function of the component should in capitalized format, means:
```jsx
function Coffee() { // First letter of the name must be capital
	return (
		<h3>☕</h3>
		)
}

export default Coffee
```

## What if we want to render more than 1 element?
In App.jsx:
```jsx
// ........
return (
	<Coffee />
	)
// ........
```
This is fine, but if we do this:
```jsx
// .........
return (
	<Coffee />
	<h3>I cannot be rendered normally 🥲 </h3>
	)
```

Its and error, because we can only return 1 component each time, so we can do this:
```jsx
//........
return (
	<div>
		<Coffee />
	<h3>I can be rendered normally 😁 </h3>
	</div>
	)
// ......
```
But it became such a common problem the react community just did this:
```jsx
// ...........
return (
	<> 
		<Coffee />
	<h3>I can be rendered normally 😁 </h3>
	</>
	)
// ......
```

```<>```: empty brackets (a.k.a. Fragment)
