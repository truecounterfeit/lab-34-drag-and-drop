####  Lab 34 Documentation

* npm run watch

* type in: localhost:8080

* Page renders a Budget Tracker Form that creates notes and displays them in a list that can be dragged and dropped by the user.

App
  Provider
    BrowserRouter
      Route / Dashboard
        CategoryForm -- for creating categories
        [Category Item] -- list of Category items
           Dropzone
             CategoryForm  -- for updating categories
             ExpenseForm -- for creating expenses
             [ExpenseItem]  -- list of expense items
                Draggable
                  ExpenseForm -- for updating an expense

###### Draggable -  a component that enable users to drag its children

###### Dropable - a component that enables users to drop a Draggable component

###### ExpenseItem - contents of the ExpenseItem in a Draggable

###### CategoryItem - a category item in a dropzone
