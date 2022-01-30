# Jewelstore (AR Jewelry E-Commerce Store)
# Problem Statement
['Homemakers in rural India hold over 11% of the actual amount of gold in the world. Consequently, Indian women collectively wear over 21,000 tons of gold on their bodies. To put this figure into perspective, the Indians’ obsession with gold has pushed them to accumulate more gold than all the reserves of the IMF, USA, Germany, and Switzerland put together.'](https://blog.novemgold.com/interesting-fact-indian-housewives-hold-11-of-the-worlds-gold/) However, almost all of the jewelry shopping is done traditionally. This is a market longing for a disruption. ['Only 7.6% of the global jewelry shopping was done online and India only had an online penetration of 1.2%'](https://retailjewellerindia.com/how-big-is-the-online-jewellery-market-in-india/). What could be the reasons of such low market penetration in online jewellery shopping? 

 - **Trust**
 *The majority of people still don't buy gold or diamonds without visiting a shop. Jewellery is a luxury purchase and is an investment for any Indian household. They don't want to take risks. They want to choose the best design, check on the purity of gold, see its make in reality and then make a decision.*
 - **Can't experience the touch and feel**
 *Not being able to try on rings and other jewelry. Not seeing the actual product to check the quality of the item you want to buy.*
 
 There could be countless other reasons and factors, but we aim at solving these two for our client **Siddhi Jewellers**. They are trusted by their clients, but what if we can elevate the trust using technology. What if we can integrate Augmented Reality with Jewellery Shopping? This idea was the motivator of this project. Combining something as fresh as AR into something as traditional as Jewellery shopping. It is undeniable that humans love hoarding jewellery. Many consider gold and diamond an investment and technology is meant to solve our problems. We aim at solving this problem using technology. 

## Probable Actors

1.  **Customer** -
    1.  View, Order, Try various jewelries available on the brochure
2.  **Owner/Admin** -
    1.  Add, Update, Delete jewelries and stocks
    2.  View Customers and Orders
    3.  View Transaction Histories

## Usecase Diagram & Descriptions

### Usecase Diagram
![AR Jewelry System](https://user-images.githubusercontent.com/40191280/151697032-cd43ebb6-a6b3-4003-82f8-1a392a943762.png)

### Usecase Descriptions

### 1 (To be reviewed)

| Use Case Name:        	|   Login	|
|-----------------------	|---	|
| Primary Actor:            	|   User	|
| Description:            	|   This use case helps the system distinguish between customer and owner	|
| Relationships:            	|   <ui>**Extends** <li>Handle Abort </li> <li> Handle Invalid Password 	|
| Triggering Event:     	|   User clicks the login button	|
| Preconditions:        	| User must be a registered as a customer or owner in the database
| Postconditions:       	|   If the use case was successful, the actor is now logged into the system. If not the system state is unchanged.	|
| Basic Flow:   	|  <ul><li>The system requests user credentials </li><li>User enters the credentials in the system</li><li>The system checks the user credentials</li></ul> 	|
| Exception Conditions: 	|   <ul><li>The credentials entered are wrong</li> <li> The user aborts login before verification|

### 2 (To be reviewed)

| Use Case Name:        	|   Try Jewelry	|
|-----------------------	|---	|
| Primary Actor:            	|   Customer	|
| Description:            	|   This use case helps the customer try  jewelries on their screen using the help of **Augmented Reality** 	|
| Relationships:            	|   <ui>**Included in** <li>Order Jewelery </li></ui><ui>**Extends** <li>Get camera permission </li> <li> Handle AR errors	|
| Triggering Event:     	|   <ui><li>Customer selects any product to try </li> <li>Customer orders any product, then they must try it before checkout|
| Preconditions:        	| <ui><li>Customer must be logged in in the system </li> <li>Customer must have a camera in their device </li> <li>Customer should be in a well lit area
| Postconditions:       	|   *None*	|
| Basic Flow:   	|  <ul><li>Customer selects the try jewelry button</li><li>System scans the customer's face </li><li>System processes and applys the *3D* jewelry model on the customer's face </li><li>Customer can proceed or run the scan again</ul> 	|
| Exception Conditions: 	|   <ul><li>System faces any problem to access the customer's camera</li> <li>Customer's face is not under adequate lighting for the algorithm to process and apply the *3D* model|
