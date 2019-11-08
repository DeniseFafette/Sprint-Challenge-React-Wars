# Sprint Challenge: React - Star Wars

This challenge allows you to practice the concepts and techniques learned over the past Sprint and apply them in a concrete project. This Sprint explored ReactJS, Function Components, component state and side effects. In your challenge for this Sprint, you will demonstrate proficiency by creating an application that uses ReactJS to consume live data retrieved from the World Wide Web and style that data nicely on the page.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency with ReactJS Fundamentals and your command of the concepts and techniques in the Functional Components.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons and your Team Lead.

## Description

In this challenge, create a web page that presents a styled list of Star Wars characters. Being able to render out data to a web page is a large part of what JavaScript developers do, this challenge assesses your ability to achieve such a task.

## Self-Study/Essay Questions

Demonstrate your understanding of this Sprint's concepts by answering the following free-form questions. Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager.

- [ ] What is React JS and what problems does it try and solve? Support your answer with concepts introduced in class and from your personal research on the web.

React JS is a JavaScript library. provide developers with the ability to build large scale applications effectively.

The core philosophy of React development revolves around creating small, reusable building blocks—components—which can ultimately be pieced together to form entire websites  Companies like Netflix, Walmart, Dropbox, Tesla, Airbnb, and many, many others use React. This wide adoption is due to React’s component-based architecture: It allows large organizations to work nimbly, introducing components as needed without completely rewriting their entire codebase.

Additionally, the introduction of React Native—a sister framework that enables cross-platform mobile app development in React-flavored JavaScript—enables development teams familiar with React on the web to easily build mobile apps as well. This means developers can work across a suite of digital products that run on different platforms but share the same codebase and the same components.

That shared understanding (and code!) across products creates efficiencies and flexibility you don’t have on a development team that has to be able to write and maintain native Android code, native iOS code, and code for the web.- Postlight.com

Because we have such rich user interfaces today that interact with ever-changing data, users interacting with DOM elements, and lots of animations and events firing, the DOM is doing a lot of work. We need a way to offload a lot of the state (data) that our apps need to use, from the DOM. To keep up with today’s demands of the web, we need a way to build applications that can take care of that workload.

Working with the DOM API is actually really hard. The React built a simple engine called the virtual DOM that interacts with the actual DOM for us. 

We simply tell the virtual DOM which elements and state (data) to render to the actual DOM, and it will do so. Beyond that, it will “react” when the state (data) in our app changes, and will update the DOM accordingly. All on its own!
In a process called “reconciliation”, React will detect that the state of the app has changed. Then it will update the virtual DOM, taking note of which nodes have changed due to the state changes. Finally, once it knows which nodes have changed, it will update only those specific nodes on the actual DOM. This takes a lot of pressure off of our browsers and it’s why React is as powerful as it is.

React solves the problem of providing a smooth experience for our users, as well as those developing applications.


- [ ] What does it mean to _think_ in react?

Being able to think in terms of components and breaking down an app into a system of components.
When we return what looks like HTML in a React component what we’re actually returning is a JavaScript object that describes the kind of HTML we want to make. A React component is just a regular JavaScript function. We use JSX for a couple of reasons. First, it’s easier to read. Second, it  allows us to put our application’s logic where it belongs: directly next to the thing the logic applies to.
two major pillars of React’s design philosophy for now. 
Separation of concerns and declarative programming.
“the separation of concerns” refers to a design philosophy that each piece of your code should do one and only one thing.
Declarative programming unlike imperative coding that uses step by step programming relies on a level of abstraction (making it program agnostic) to program what to do. In declarative coding  we are  describing WHAT we want to happen rather than HOW (we don’t know HOW map and reduce are implemented, we also probably don’t care). We’re not mutating any state. All of the mutations are abstracted inside of map and reduce.
 
myArray.map(double)
“Map over my array and double everything inside of it.”
With practice declarative code is easier to parse. This is really important because, believe it or not, as a programmer, most of your time isn’t actually spent writing code. It’s spent reading other people’s code and trying to understand what it does. If you can grasp this distinction, and appreciate its value, congratulations. You now understand the basis of functional programming, the programming paradigm that React is modeled on.
JSX is an XML/HTML-like syntax used by React that extends ECMAScript so that XML/HTML-like text can co-exist with JavaScript/React code. ... Unlike the past, instead of putting JavaScript into HTML, JSX allows us to put HTML into JavaScript.


- [ ] Describe state.

One of the single most important concepts in programming: state. React components has a built-in state object. The state object is where you store property values that belongs to the component. When the state object changes, the component re-renders. So the state determines how that component renders & behaves. This allows developers to create components that are dynamic and interactive.
WC3 Schools Example:
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {brand: "Ford"};
  }
  render() {
    return (
      <div>
        <h1>My Car</h1>
      </div>
    );
  }
}


- [ ] Describe props.

In a React component, props are variables passed to a component by its parent component. State on the other hand is still variables, but directly initialized and managed by the component.
We never make changes to props data - props are read only. This helps insure that our data flow remains clean and organized. This way when changes are made to our application we know where. And if something goes wrong, we can find the issue and fix it.


- [ ] What are side effects, and how do you sync effects in a React component to state or prop changes?

A side effect is anything that affects something outside the scope of the function being executed. Fetching data from an API, timers, logging, and manually manipulating the DOM are all examples of side effects. 
A React component without side effects is called a pure component. A component can be considered pure if it renders the same output for the same state and props.
A side effect is something that can cause a component to return a different output for the same state and props. React offers us tools for managing side effects so we can avoid bugs and inconsistencies in our app. The effect hook (useEffect()) is one of those.

Using a dependency array as the second argument in the effect hook, we can tell it with which state or props the effect should be synced. This is a handy guide to use as you begin the build the mental model for this principle:
… the question is “with which state and props does this effect synchronize with”


## Project Set Up

Follow these steps to set up and work on your project:

- [ ] Create a forked copy of this project.
- [ ] Add TL as collaborator on Github.
- [ ] Clone your OWN version of Repo. **(Not Lambda's by mistake!)**
- [ ] Create a new Branch locally: `git checkout -b <firstName-lastName>`.
- [ ] Change directories into `./starwars` (`cd starwars`) and run `yarn install` or `npm install` to retrieve all needed dependencies.
- [ ] Once you have installed the _node_modules_, run `yarn start` or `npm start` to get your server up and running.
- [ ] With the server up and running, open Chrome and head over to `localhost:3000` and view your beautiful app. Maybe it's not _that_ pretty... _yet_, your goal is to ensure this project becomes a thing of beauty.
Follow these steps for completing your project.
- [ ] Implement the project on this Branch, **committing progress & changes often.**
- [ ] Push commits: `git push origin <firstName-lastName>`.

Follow these steps for completing your project:

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo).
- [ ] Add your Project Manager as a Reviewer on the Pull-request.
- [ ] PM then will count the HW as done by merging the branch back into master.


## Minimum Viable Product

Your finished project must include all of the following requirements:

- [ ] Fetch a list of Star Wars characters from the [Star Wars API (or SWAPI)](https://swapi.co/) and render them to the screen. 
- [ ] Follow the documentation to learn how to fetch a list of "people". However, don't spend _too_ long on this. Here is a link for you to follow if you've looked around the docs for about 15 minutes or so and haven't found where to go - [Secret Link to Awesomeness 🤫](https://swapi.co/documentation#people).
- [ ] Set the data you fetch to state.
- [ ] Map over the list and render a component for each character on the page.
- [ ] You must display at least one element for each star wars character in the data set.
- [ ] The elements must be styled with either Reactstrap or styled-components - don't rely on browser default styles.

#### Required best practices:

- [ ] Consistent naming. Examples: variables, functions, Components, and file/folder organization.
- [ ] Consistent spacing. Examples: line breaks, around arguments and before/after functions.
- [ ] Consistent quotation usage.
- [ ] Spell-check.
- [ ] Schedule time to review, refine and reassess your work.


It is better to submit a challenge that meets [MVP](https://en.wikipedia.org/wiki/Minimum_viable_product) than one that attempts too much and fails.

## Stretch Problems
- [ ] Next week we will be looking at React forms. Look a head and try to create a search form that will filter through the data displayed from your characters. 

- [ ] Build a pagination system that will allow you to load the next page of data.
  - `console.log()` the data coming back from the server.
  - Notice that there are `next` and `previous` fields that give you a URL.
  - You can build a function that will get characters called `getCharacters` that you can use dynamically to get the next or previous set of characters. You would need to supply it with the proper fields, and you'll need to set up more state to do this.
  - [ ] Add at least one test using a testing tool:
  - [react-testing-library](https://github.com/testing-library/react-testing-library#basic-example)
  - [Cypress](https://docs.cypress.io/guides/overview/why-cypress.html)

<!--
- [ ] Build another app from scratch that looks very similar to this one. Inside of your main `App` component fetch some data in this same fashion from this url `https://dog.ceo/dog-api/#all` you'll have to follow the documentation at that website and figure out how to change up the code you've seen here in this Star Wars app in order to properly fetch the data and store it on Component State.
-->
