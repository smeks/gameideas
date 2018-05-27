# Software Consultant Inc
Solve puzzles by taking information from systems and integrate them into custom business solutions.

2D game with components the user will extend and connect.  Creating connections generates additional connectable nodes.  For example a new function on the server is created when the server is connected to a field in the database which then can be connected to other parts.

## Puzzle #1 Display employees
```
### available components to use
	1. database with several tables
	2. server module
	3. app module
	4. app text control

### steps to win
	1. create app text control in app
	2. connect employee name field from database to the server (creates ServerGetEmployee)
	3. connect ServerGetEmployee to the app (creates AppGetEmployee)
	4. connect AppGetEmployee to the app text control

### win scenario
	app displays employee names
```
## Puzzle #2 Add employee
```
### available components to use
	1. database with several tables
	2. server
	3. app
	4. app text field
	5. app button

### steps to win
	1. create app text field
	2. create app button
	3. connect server to employee name in database (creates ServerCreateEmployee)
	4. connect app to ServerCreateEmployee (creates AppCreateEmplyee)
	5. connect app button to AppCreateEmployee
	6. connect app text field to AppCreateEmployee

### win scenario
	app creates new entry in database in the employees table when text is entered into text field and button is pressed.
```