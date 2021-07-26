# Car-rescue-app-webservice

Application for car rescue when it breaks down on the way, rescue is either by delivering to the car owner (client) nearest winch or nearest mechanic. <br />
We used Nodejs as our programming language, ExpressJs framework, Mongodb and Restful API. <br />
The project is 3 applications; customer app, winch driver app and mechanic app. <br />
- My role: I worked in the backend side.
# The Functional requirments of the project:
# Customer application:
1. Login: with Mobile number or facebook account
2. Signup: with mobile / facebook account
3. Choosing which service (Winch/Mechanic)
4. Booking:
a. Requesting Service:
 Winch request: Info about from where,to where the trip will be
determined(+suggesting closest maintenance centers client can go to)
 Mechanic Request: Only the client’s location will be determined
b. Matching process:
c. Nearest winch/mechanic will be matched with client
d. Service confirmation :
e. Duration estimation+fare estimation+payment method
5. Driver/Mechanic tracking:feature to observe their movement to make updates
6. Payment procedure:multiple payment variants may be implemented; cashless -
in-app payment via credit cards, or simply in cash
7. Review & Rating: corresponds to the service evaluation
8. Trip cancelation
9. Booking history: Shows details from previous rescue-services provided.
# Mechanic/Winch Driver application:
1. Sign up: Mobile number and needed Documents are provided in a form to
be reviewed by admins
2. Login: with username,password/facebook account
3. Mechanic/driver status ( Availability ): Chooses online/offline state
4. Rescue alert+confirmation/denial: Ability to receive rescue service orders
to accept or deny, including information regarding client’s location, route,..
6. Navigation & route optimization: Offer the best route using Google Maps.
7. Repairs/Spare parts used checklist: Mechanic checks the fixations he has
made and spare parts used to enable the app determine the final fare. (Only for mechanic app)
8. Service history
9. Review for client: Mechanic/driver rates the client.
#  Non Functional requirements: ( which are related to the backend side)
1. All apps support both Arabic & English Languages.
2. The web service using node js.
3. The authorization is done using JWT tokens which are very secure and cannot be forged.



