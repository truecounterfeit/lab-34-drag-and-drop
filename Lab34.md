401 JS --  Lab 34 Budget Tracker
===

Unlike the previous React assignments where you have been shepherding your work through the labs, for this assignment, you have been given a starting point from which to begin.

Assume you have been hired at a company and have been handed this codebase, and need complete the project for delivery.  You must work from the existing code, adopting it's style, layout and architecture while still fulfilling the requirements.

Further assume that what you have here is already in production as a "Phase 1 or 2" and you are implementing the final set of requirements. Be sure not to "break" any existing functionality.

## Submission Instructions
  * Begin with a fork of this repository
  * submit a pull request to the project

## Requirements  
#### Feature Tasks
* complete the lab 31, 32, and 33 tasks
* This should demonstrate the totality of: Reducers, Combined Reducers, Middleware, Logging, Validation, Drag and Drop, Testing (Unit and Component)

##### SCSS
Style the application using sass best practices  
 * Create a _reset.scss _vars.scss and _base.scss
 * style your components

##### Components
add and refactor  the following components and organzie them according to the following tree
```
App
  Provider
    BrowserRouter
      Route / Dashboard
        CategoryForm -- for creating categorys
        [Category Item] -- list of Category items
           Dropzone
             CategoryForm  -- for updating categorys
             ExpenseForm -- for creating expenses
             [ExpenseItem]  -- list of expense items
                Draggable
                  ExpenseForm -- for updating an expense
```
###### Daggable
* Create a component that enable users to drag its children
* It store data passed into its `dataTransferItem` prop on the event handler for `onDragStart`
  * data should be stored as json under the MIME 'application/json'

###### Dropable
* Create a component that enables users to drop a Draggable component
* onDrop it should invoke a callback with the data passed using the events dataTransferObject
  * remember to parse the json


###### ExpenseItem
* Wrap the contents of the ExpenseItem in a Draggable
* Pass the expense data into the Draggables dataTransferItem prop
* Implement field level validation for your expenses (title, amount required and properly typed)

###### CategoryItem
* Wrap the contents of a category item in a dropzone
* When the onComplete of a Dropzone is fired update the expense so that it appears on the correct category
* Implement field level validation for your categories (title, amount required and properly typed)


#### Test
* Test every component except app
* Test all of your action creators
* Test each reducer used in your apps combineReducers
  * test that the validation is working!

####  Documentation  
Write a description of the project in your README.md
