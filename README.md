# React Drills

## Passing state as props and Updating state on the parent component

<img src="https://github.com/Rasbandit/React-Drills/blob/master/images/React-double-box.jpg" />

Create an App using create-react-app that resembles the image above. The green boxes are is a single component rendered twice. The blue box represents the main component or App.js. 

### Step 1
App will have state with one property, title. Display title on the screen and have an input box below it. The input box should also display the current state of title. When the user types into the input it will update the title for App

### Step 2
Create a second component. Give this component its own state of title that gets its initial value from App as a prop.
the box should have an input box and a button.
when the user types in the text box it will update the value of title for just that component, not the parent or sibling.

### Step 3
When the user clicks the button in the child component it will update the parent component's state with the new value passed up from the child.

### Step 4
Modify the child component so that when it updates the parent component's state the other components will have its title state update also.

## Whose that pokemon!!!

<img src="https://github.com/Rasbandit/React-Drills/blob/master/images/pokemon.jpg" />

The end goal is to make a react app that has 3 rotues. To to search for pokemon by their number, one to show more details about the pokemon, and the third will show a list of all pokemon by a certain type.

If you click the Pokemon logo on top it should link back to the search page

If this intimidates you a bit, you could split this into 3 mini projects to practice HTTP requests

### Step 1: search page

make a component that has an input box and a button. The user should be able to type a number into the input box and when the button is clicked it will show the image and name of the pokemon in a child component (there is about 500 pokemon)

HTTP: `http://pokeapi.co/api/v2/pokemon/1` is the API to get pokemon, where the nubmer at the end specifies which one you want to get.
(hint: when you get a response from the server the name can be found on .data.name and the image can be found at .data.sprites.front_default)

Routing: when the user clicks the name or the image it should route them to the details page with the id of the pokemon as the url paremeter

Challenge: make it so when this page loads it will pick a random number from 1-500 and show that pokemon

### Step 2: Details page

The component should show the same pokemon on this page as the one you searched, passing that info in from the URL parameter. Have this route show as much information about the pokemon as you want, but make sure to list the types of pokemon that it is.
(Hint: the types can be accessed from the HTTP response by accessing data.types. the types is an array with sometiems one item and sometims two)

Routing: When the user clicks one of the types route them to the types page with that type (eg: fire, ice, water, grass) in the URL Parameter

### Step 3: Pokemon by Type

This page will show all pokemon based off of the type parameter in the URL. You can make an API call to the Pokemon API to get that information.
`http://pokeapi.co/api/v2/type/fire`
Just change out the last part where it says fire to what ever type you want and it will return a list of that type.

Routing: Make it so when you click the name of the pokemon it links back to the details page and it will show that pokemon and its unique info

Challenge: make it so the text color changes based off the type, eg: red=fire blue=water green=grass