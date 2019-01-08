![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## Project Name

### Author: Student/Group Name

### Links and Resources
* [repo](https://github.com/Kevinoh47/lab-33)
* [codesandbox](https://codesandbox.io/s/5z8vknm17n)


### Modules

#### `if.js`
##### Exported Values and Methods

#### `list.js`
##### Exported Values and Methods

#### `modal.js`
##### Exported Values and Methods

#### `person.js`
##### Exported Values and Methods


#### `thunk.js`
##### Exported Values and Methods
The /src/store/middleware/thunk.js exports a curried function which calls the store, then next, then action, before testing that action to see whether or not the action is itself a function. If it is, thunk calls that function with store.dispatch() and store.getState() functions as input parameters. 

By injecting this code between the invocation of the action and the action itself, asyncronous calls such as API calls can be made and managed before the action executes and returns.  

#### `people-actions.js`
##### Exported Values and Methods
The /src/store/actions.js file exports a get function which takes a url, dispatches it to the store (via thunk I believe), and then runs the utis.fetchData(url) function, which returns a promise. 

With the data returned from the async call, a further, internal function called runAsyncGetAction is called to run the action, ultimately returning an object with type of action (e.g., "GET") and the payload.

#### `person-actions.js`
##### Exported Values and Methods
The /src/store/actions.js file exports a get function which takes a url, dispatches it to the store (via thunk I believe), and then runs the utis.fetchData(url) function, which returns a promise. 

With the data returned from the async call, a further, internal function called runAsyncGetAction is called to run the action, ultimately returning an object with type of action (e.g., "GET") and the payload.

#### `index.js`
##### Exported Values and Methods
The /src/store/index.js file builds the Redux store and exports the createStore function.


#### `people-reducers.js`
##### Exported Values and Methods
The /src/store/reducers.js file exports a function which manages state by checking the type of action expected, and returns what is expected of that action. In our case we are switching between a "GET" action which returns the payload, and a default action which just returns state.

#### `person-reducers.js`
##### Exported Values and Methods
The /src/store/reducers.js file exports a function which manages state by checking the type of action expected, and returns what is expected of that action. In our case we are switching between a "GET" action which returns the payload, and a default action which just returns state.

#### `app.js`
##### Exported Values and Methods
The /src/app.js file builds and exports App, connected to the store via mapStateToProps and mapDispatchToProps. The App class manages its own state as well as attaches to the store. It uses the store to get a list of people via props. Because I could not figure out how get the store to store and supply drill down data on each person, I had to use local state to store selected person data for rendering drill down data. If a person is in the local state, drill down data is rendered as well as the initial list of persons.

#### `index.js`
##### Exported Values and Methods
the /src/index.js is the entry point into the application, building athe Main class, which wraps the App component in the store provider, allowing all child components access to the store.

### Setup


#### Running the app
* Endpoint: `https://5z8vknm17n.codesandbox.io/`
  * Returns the app.

#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events
