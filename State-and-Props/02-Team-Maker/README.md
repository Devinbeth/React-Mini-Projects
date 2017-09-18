# Team Maker

This app aims to improve your skills in using a .map loop to create JSX elements and using setState to add members to an array on state. Eventually we will move our code into component to clean up our code and make it more maintainable.

The end result will hopefully look some thing like this

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Team Maker/Team-Maker.jpg" width="375" height="400">
</p>


## Starting Point
#### Creating the React App

With your terminal opened inside of this folder, `02-Team-Maker` run the following command into your terminal to create the project.

`create-react-app Team-Maker`

This will give you a blank slate to create your react project. You will want to start in the `App.js` file.

## Phase One
#### Using an Input to Change State

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Team Maker/phase-1.jpg" width="375" height="420">
</p>

In our app we want to give the user the ability to type a name into an input field and save them to a team. To start lets begin with creating a function that will update our state and save a title for our app.

You will need to create a constructor function in your `App.js` and create your initial state. The initial state should have a property of title, and any string value you like. Display the current value of title from the state on the browser inside your JSX section.

You will also need to create a function that will run every time the user types in the input box. This can be done using an on onChange on the input JSX tag.

If everything is working correctly when you type in input field it should live update the title at the top of the page.

#### Phrases to Google for help
- React onChange
- React Forms

#### Projects with example Code
- Toy Problem Showcase

## Phase Two
#### Update Title Only when Button is pressed

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Team Maker/phase-2.jpg" width="375" height="420">
</p>

In this step we will change our app so that the title will only update when we press the save button. Create a button in the JSX section.

We will need to create a second property on our state that will keep track of what is in the input, but we need to keep it separate from the value storing the current title. The reason for this is so we don't update the value for team until we type in the whole name. We will be doing the same pattern for adding team members, as we don't want to add a team member each time a key is pressed, that would give us an array full of half finished names.

You may also want to make it so when the user clicks the save button it clears the input field and sets the value on state for storing the input to an empty string.

#### Phrases to Google for help
- React onClick
- React setState Example onClick

#### Projects with example Code
- Employee Manager (Employee Editor Component)


## Phase Three
#### Using .map to show a list of items in JSX

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Team Maker/phase-3.jpg" width="375" height="420">
</p>

Change the title on the top of the app so that it is static and not reflecting what is on the state, but move the value from state to below the input boxes so we can still show the name of our team.

You you will need to create a new input field and button to handle adding team members to our team list. This also means you will need a place to keep track of this info. On state create an array to hold the members of our team. when the user clicks the save Team Member button it will add their name to the array of team members as a string.

Using array.map inside of the render method, but outside of the return, loop through the team members array and make a JSX tag for each member of the array. Put the variable you made to store each team member down in your return.

#### Phrases to Google for help
- React map array
- React setState array example onClick

#### Projects with example Code
- Employee Manager (Employee List Component)


## Phase Four
#### Creating a component and passing props

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Team Maker/phase-4.jpg" width="375" height="420">
</p>

In this phase lets convert our team title and list into a component. This makes it easy to repeat our code for when we want to add a second or even third team.

You will need to create a new component and transfer over your map function in your render method as well as any JSX for styling purposes. When you implement your component into App.js you will need to pass down two props, the team title and the team list. Remember you can access your props inside your component by using `this.props.THE_NAME_OF_THE_PROP`.

You will want to use props to set your initial state so that each component will have its own unique state. This also means you will need to use the `componentWillReceiveProps` life cycle method to update state when the props updates.

#### Phrases to Google for help
- React pass props to child
- React creating a component
- React componentWillReceiveProps

#### Projects with example Code
- Theme Changer

## Phase Five
#### Using the same component to display two teams

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Team Maker/phase-5.jpg" width="375" height="420">
</p>

Lets duplicate our code so that we can create and manage two teams at the same time. You will need to add another team on your App.js' state and another spot to hold a team name. Create another instance of your team list component and pass it the the values for the new team and team name. 

You will also need to create a new team member box and button, as well as team name box and button and set them to update the new values on state.

## Phase Six
#### Migrating all info into the component

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Team Maker/phase-6.jpg" width="375" height="420">
</p>

You may have realized already but having our app manage the state for the two teams is not the most effective way. It would be better if the component had the input boxes inside of the component itself. This would make it so we could add a whole new team without having to keep making info on our App.js

In this step move the team member and team name input's into the component and have it change the components state instead of using props and `componentWillReceiveProps`.

If you moved the input fields to the component correctly you should be able to create copy the component as many times as you want and each component will be able to keep track of its own state.