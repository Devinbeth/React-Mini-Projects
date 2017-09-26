# Button Clicker

The goal of this project is to create an app from scratch that will track the number of clicks on a button.
we will be using setState to modify the state of a component and eventually create a child component that will be able to modify the parent state through a function passed to the child through props.

The end project will look a little something like this.

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/Clicker.jpg" width="350" height="425">
</p>

## Image Explanation
In the images below the green box represents the `App.js` component and any white boxes represent div's or other html tags. Blue boxes represent Child components

## Starting Point

### Creating the React App

With your terminal opened inside of this folder, `01-Clicker` run the following command into your terminal to create the project.

`create-react-app clicker-app`

This will give you a blank slate to create your react project. You will want to start in the `App.js` file.

## Phase One

### Connecting a button to JavaScript

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-1.jpg" width="350" height="425">
</p>

The green box in the image above represents the App component. For this step we will not need to make any children components.

Write a method(AKA function) on your class that will console log a message to the browsers terminal when ran. Using the `onClick` event handler run the method you made. You will need to use an `arrow function` on the `onClick` to get this to work. Once you get this working and you can see the console log in the inspect window of your browser we can move onto tracking how many times it has been clicked.

#### Phrases to Google for help
- React onClick
- js creating a method on a class

#### Projects with example Code
- Calculator
- Toy Problem Showcase


## Phase Two

### Updating State

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-2.jpg" width="350" height="425">
</p>

In this step we will be adding state to our App component that will allow us to track how many times we have pressed the button.

Create a constructor function inside the class component and create a value called `this.state`. `this.state` is an object and should have one property on it called `count`, and be default it should be set to 0.

Render that value of count in the JSX so the user can see the total.

Change the logic of your function that console logged when the button clicked. We need to run the setState function to update the value of count.

If everything is working you should see the number on the screen increment every time you click the button.

#### Phrases to Google for help
- React setState example

## Phase Three

### Making Another Button
<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-3.jpg" width="350" height="425">
</p>

In this phase you will create a second button that will decrement the number by one.

You could create a separate function to handle the subtraction, but our code would be easier to maintain if it took in a parameter (being the number to either add or subtract from the total) and it would modify our state's number by the amount passed in. Doing it this way would save us from having to write multiple functions.

#### Projects with example Code
- Calculator

## Phase Four

### Making More Buttons

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-4.jpg" width="350" height="425">
</p>

Similar to phase four but we will add two buttons that will increment by 5 and decrement by 5. Your code will be most effective if you dont need to make additional functions for each button but instead run the same function but pass it different values.

## Phase Five

### Buttons to Components

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-5.jpg" width="350" height="425">
</p>

In this step we will create a button component that will take the place of our individual buttons. You will only need to create one new component but we will use the same component 4 times and pass each one a different prop, being a number. This number will be how much the total will increment by and the number to be displayed on the button. By converting our button into a component it makes it easier to make changes to all the buttons at once and easier to create more buttons if needs be.

You will need to give each component two props, the function (make sure you bind this function inside of the constructor) and the value to increment/decrement by. Inside of your component you can access the props by using `this.props` If you are unsure what `this.props` is, you can always console.log it inside your render method, but outside of the return.

This component will not need its own state, meaning it will not need a constructor function.

#### Projects with example Code
- Theme Changer

#### Phrases to Google
- React passing props
- React accessing props
- React biding functions
