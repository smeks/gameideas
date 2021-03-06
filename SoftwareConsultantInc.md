# Software Consultant Inc
Solve puzzles by taking information from systems and integrate them into custom business solutions.  It would function similar to shenzhen io but without any programming and more focused about integrating between different systems to solve practical business requirements.

It would be a 2D game with many simple components the user will extend and connect to create a very complex system.  Creating connections generates additional connectable nodes.  For example you can define a data component in the app with some simple data elements.  Connecting the data component from the app to the server will generate methods to communicate the data between the app and the server and the definition will be on the server that can be used further.

Another example; taking a very slow process and splitting it up into several queued jobs that work on one small thing at a time and taking the output of one process as input into another.


## Puzzle #1 Display employees

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

	
## Puzzle #2 Add employee

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
	
	
## Puzzle #3 Saved Shopping Cart Checkout

Create an app that takes a users shopping cart information, totals the item prices, send total for payment processing and creates a purchased record for the shopping cart items.

### available components to use
	1. Database
	2. Server
	3. Sum
	4. Payment
	5. App
	6. Data
	7. Button

### steps to win
	1. create "Sum" component in "Server"
	2. create "Payment" component in "Server"
	3. connect existing "ShoppingCartData" component under "App" to "Server" (creates "AppPay" & "ServerPay" server components)
	4. connect app button to "AppPay"
	5. connect "ItemPrice" in "ServerPay" to "Sum" in server (creates "SummedItemPrice" under "Sum")
	6. connect "SummedItemPrice" to "Payment" (creates "PaymentSuccess" and "PaymentFailure" data components)
	7. connect "ShippingCartID" under "ShoppingCartData" to "PaymentSuccess" and "PaymentFail" data component (combines data)
	8. connect "PaymentSuccess" to "Purchase" table in database
	9. connect "PaymentFail" to "PurchaseError" table in database
	

### win scenario
	app sends ShoppingCartData to server and item total is summed and sent for payment.  successful payment is logged as a purchase.  failed payment is logged as a purchase error.