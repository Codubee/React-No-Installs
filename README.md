# Lets build some components!

## Step 1: Add scripts to our head tag to download react, babel, and React DOM to our index.html page

```html
<script src="https://unpkg.com/react@16/umd/react.development.js"></script>

<script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>

<script src="https://unpkg.com/babel-standalone@6.26.0/babel.js"></script>
```

## Step 2: Replace the existing HTML code in the body with the following

```html
<div id="root"></div>
```

## Step 3: Add a script in the head tag with the type being text/babel

```html
<script type="text/babel">
      // React code will go here
</script>
```

## Step 4: Create a functional component


In the script tag we just created:
- Use the function keyword to create a functional component
- Give the function a name of Welcome
- Return an h1 element that says hello world from functional component

```javascript
function Welcome(){
      return <h1> Hello World from functional component</h1>
}
```


## Step 5: Render the functional component

In the same script tag where the Welcome component exists, write the Render function
```javascript
ReactDOM.render(<Welcome />, document.getElementById('root'))
```

## Step 6: Create a class component

In the same script tag we used before:
- Use the **class** keyword to create a class component
- Give the class component a name of WelcomeClass
- Make sure to extend React.Component
- Write a render function that returns an h1 element that says Hello world from class component
```javascript
class WelcomeClass extends React.Component{
      render(){
            return <h1>Hello world from class component</h1>
      }
}
```
## Step 7: Render the class component

- Make sure to surround the components with a parent div
```javascript
ReactDOM.render(<div>
<Welcome />
<WelcomeClass/>
</div> , document.getElementById('root'))
```
## Step 8: Add props

Using the functional Welcome component
- Add a prop of **name** and a value of **Gatsby** to the Welcome functional component
``` javascript
<Welcome name="Gatsby"/>
```
- Add props to the parameter of our functional component
``` javascript
function Welcome(props)
```
- Use the props to display the **name** prop
``` javascript
return <h1> Hello {props.name} from functional component</h1>
```

## Step 9: Add state
- Add the constructor method to our class component and make sure to call the super class as well
- Inside of the constructor, create a state object with a key of name and a value of Athena
``` javascript
constructor(){
      super()
      this.state = {name:'Athena'}
}
```
- Use this.state.name in the render method to display the name
``` javascript
render(){
      return <h1>Hello {this.state.name} from class component</h1>
}
```

