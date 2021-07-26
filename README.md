# Car-rescue-app-webservice

Application for car rescue when it breaks down on the way, rescue is either by delivering to the car owner (client) nearest winch or nearest mechanic. <br />
We used Nodejs as our programming language, ExpressJs framework, Mongodb and Restful API. <br />
The project is 3 applications; customer app, winch driver app and mechanic app. <br />
- My role: I worked in the backend side.

# Backend Implemtation steps :
- The web service and the mobile app both communicate together through a RESTful API. The authorization is done by using JWT Tokens which contains the data for each respective user and the user type. <br />
- The process mainly is about 3 stages: <br />
 1. Users Registration (Customer, Mechanics and Winch)
 2. Adding new cars.
 3. Requesting a rescue
- AUTHORIZATION IS REQUIRED IN ANY STEP OF THESE 3 STAGES <br />
1) Registration: process goes through the following steps respectively: <br />
- Validation of data
- Validates the mobile number on the firebase and date.
- Returning the proper JWT token which has the user id and the user type and a few more data used by the app. <br />
This is the registration for customer, registration for mechanics and winch drivers is a similar process to that of the customer but added to that is the required papers         upload like the driving license, national id and so on. The request is then sent to the server for review and being approved by one of the admins after reviewing the papers
through the admin panel. <br />
2) a. Adding new cars: First time the user logs in a list of all the cars is being sent to the mobile. It sends an array of the cars that are registered on the site. <br />
   b. Loading the customer’s car: It is done on login by sending a list of the customer’s cars. The request contains the following data:- CarId - Brand - Model - Year of make -    OwnerId - Plates.
3) Making request from client-side and mechanic/winch driver accepting the request: The matching is done based on the shortest distance and then time of arrival of the driver. The web service makes use of the Google Maps API to get the distance and time.
3.1. Creating a new request from CLIENT-SIDE either winch/mechanic request (each request has its parameters that will be sent as,pickup Location,dropoff location, initial diagnosis to the car,..).
3.2. Request from MECHANIC/DRIVER-SIDE to get matched with nearest client and accepting the request he gets matched with.
C. Checking the request status from CLIENT-SIDE , response to the request: searching status, accepted status, termibated ,..
D. Cancelling Request from CLIENT-SIDE.
E. Live tracker to Update Location to MECHANIC/DRIVER-SIDE.
F. Cancelling Request from MECHANIC/DRIVER-SIDE.
G. Winch driver/mechanic arrival at customer's location.
H. Winch driver/mechanic service start.
I.  Problems that can face the customer ( he can send them to us as initial diagnosis),services mechanic can provide him, items that he can buy to his car are added to the database (In mechanic request case)
J. problems, services, items can be loaded on the applications. (In mechanic request case)
K. Mechanic choosing Repairs that the car needs either service to be made or item to be put in the car
L. Customer display for chosen Repairs to approve them
M. Ending the winch ride 
N. Fare Calculation
0. Rating for both sides customer,mech/driver
P. Adding requests logs to the database
- Those are considered to be the FUNCTIONAL REQUIREMENTS of the project.
- NON-FUNCTIONAL REQUIREMENTS: ( which are related to the backend side)
1. All apps support both Arabic & English Languages.
2. The web service using node js.
3. The authorization is done using JWT tokens which are very secure and cannot be forged.


