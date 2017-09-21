# Painting Gallery

The Goal of this project is to get you more comfortable using .map to create multiple JSX tags, and passing info between two child components. We will also be passing a function down as a prop to children components to change the state of the parent, this also means you will need to use componentWillReceiveProps.

The end result will hopefully look something like this.

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Painting Selector/Painting-Gallery.jpg" width="375" height="421">
</p>

## Starting Point
### Creating the React App

With your terminal opened inside of this folder, `03-Painting-Gallery` run the following command into your terminal to create the project.

`create-react-app Painting-Gallery`

This will give you a blank slate to create your react project. You will want to start in the `App.js` file.

## Phase One
### Using a .map to display a list from an object

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Painting Selector/phase-1.jpg" width="375" height="421">
</p>

Inside this project there is a file that came with the repo called Paintings. It has an array full of objects with information about each painting. Copy the content of the array and put it on your state in the App's constructor function. You can either use that array or make your own array with similar values.

Using array.map inside of the render method, loop through the paintings array and make a JSX tag showing the title for each painting on the array. Keep in mind that each item of the array is an object so you will need to use . notation to pull the title off each element.

#### Phrases to Google for help
- React map array of objects

#### Projects with example Code
- Employee Manager (Employee List Component)
- 02-Team-Maker

## Phase Two
### Using an onClick to display a Title

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Painting Selector/phase-2.jpg" width="375" height="421">
</p>

For this step we will be getting things in place so we can click on a title and show all the information on the selected painting. You will need to add another property onto state to hold and keep track of the last selected painting. This should be an empty object by default.

Write a function that when clicked will take in the whole painting object and set it on state as the selected painting. You will need to use this.setState. 

Modify your .map so that each title now has an onClick event handler. set the onClick equal to a fat arrow function and when it runs execute your function to change the selected image and pass in the whole painting object.

In your JSX section you will want to display the title of the selected painting to get feed back that when you click a title it displays the correct one.

#### Phrases to Google for help
- React onClick inside map

#### Projects with example Code
- Employee Manager


## Phase Three
### Displaying the rest of the painting info

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Painting Selector/phase-3.jpg" width="375" height="421">
</p>

Now that we have our onClick working and showing the title of the selected painting lets display the rest of the information on the painting object. For most of the content you can follow the same pattern as you did with displaying the title. 

You will need reference the image url inside the image's src property.

#### Phrases to Google for help
- react display image from variable

#### Projects with example Code
- Employee Manager

## Phase Four
### Changing the values on each Painting

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Painting Selector/phase-4.jpg" width="375" height="421">
</p>

In this phase we will write in the ability to change each value on the selected painting. We will need to make a funciton that will be able to update each individual value, minus the Image itself.

This means you will need use input fields instead of just displaying the values. Set the value to each input box to its corresponding info, this is done using the value property on the input tag. You will also need to add an onChange event handeler to each input and connect it to the function that updates the correct value on state.

When writing the functions to update the values keep in mind you don't want to just modify the selected painting on state, you will also need to update the item in the list of Paintings as well, otherwise when you click onto a new painting the values will not be saved.

This means you will need to loop through the array of all paintings and update just the one painting on the list.

#### Phrases to Google for help

- react update single item in array

#### Projects with example Code

- Employee Manager


## Phase Five

### Making the two section into components

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Painting Selector/phase-4.jpg" width="375" height="421">
</p>

Finally lets convert the two sections of our project into components. The list component will need you to pass it the list of paintings and the function to change the selected painting. Make sure you bind the function.

On the individual painting component you will need to pass down the selected paining component and the functions to change each value. Again make sure you bind those functions.

If everything is working properly then when you change values on a painting then swap to another paining and come back to the modified one the changes should still be there. Also if you change the name of the title it should update on the list.