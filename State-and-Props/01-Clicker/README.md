# Button Clicker

The goal of this project is to create an app from scratch that will track the number of clicks on a button.
we will be using setState to modify the state of a component and eventually create a child component that will be able to modify the parent state through a function passed to the child through props.

The end project will look a little something like this.

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-1.jpg" width="200" height="400">
</p>

## Phase Zero
#### Starting your project
While inside of this folder run the following command into your terminal to create the project.

`create-react-app clicker-app`

This will give you a blank slate to create your react project.

## Phase One
#### Connecting a button to JavaScript

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-2.jpg">
</p>

The green box in the image above represents the App component. For this step we will not need to make any children components.

Using the `onClick` event listener run a function that will console log a message. This will help us establish that our button is working so we can move onto tracking how many times it has been clicked.

#### Phrases to Google for help
- React onClick
- js creating a method on a class

#### Projects with example Code
- Calculator
- Toy Problem Showcase


## Phase Two
#### Updating State

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-2.jpg">
</p>

In this step we will be adding state to our App component that will track how many times we have pressed the button.

Create a constructor function inside the class component and create a value called `this.state`. `this.state` is an object and should have one property on it called `count`, and be default it should be set to 0.

Render that value of count in the JSX so the user can see the total.

Change the logic of your function that console logged when the button clicked. We need to run the setState function to update the value of count.

If everything is working you should see the number on the screen increment every time you click the button.

#### Phrases to Google for help
- React this.setState example

## Phase Three
#### Making Another Button
<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-3.jpg">
</p>

In this phase you will create a second button that will decrement the number by one.

You could create a separate function to handle the subtraction but the function would be a lot more useful if it took in a parameter and it would modify our state's number buy the amount passed in. That would save us having to write multiple functions.

#### Projects with example Code
- Calculator

## Phase Four
#### Making More Buttons

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-4.jpg">
</p>

Similar to phase four but we will add two buttons that will increment by 5 and decrement by 5. Your code will be most effective if you dont need to make additional functions for each button but instead run the same function but pass it different values.

## Phase Five
#### Buttons to Components

<p align="center">
  <img src="https://github.com/Rasbandit/React-Drills/blob/master/images/Clicker/phase-5.jpg">
</p>

In this step we will convert our buttons to components. To do this you will need to make a new file and set up the basics for creating and exporting and import. Make sure you import both React and Component.

When you implement the components to your JSX you will only need to pass two props; the increment function (make sure you bind this function inside of the constructor), and the number to increment/decrement by.