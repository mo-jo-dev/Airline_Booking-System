# Airline_Booking-System

## About
This is the Backend System for an Airline Ticket Booking System which has functionalities of Authorisation, Authentication, Booking, Automatic Reminder's etc. This project consists of different Microservices. There is a difference in the functions and tasks of each microservice. Each Microservice has a similar folder structure that can be explainde by different layers i.e.
- Models -> This file contains the basic design of our database.
- Repository Layer -> The files inside this layer/folder are responsible for communicationg with the model file or with the database.
- Service Layer -> This layer has all the main business logic and it interacts with the Repository layer.
- Controllers -> This is the bridge between Front End and Backend. The requests received from frontend are received here
- Routes -> This folder contains the details of events that occur when we hit a API. This is based on REST Conventions and is resource oriented.
- Middlewares -> To prevent any misinformation, or less information, this is a layer that looks into that  matter. For example is there is no password while signing in, then this layer will directly send error response that information is not complete.

## Tasks and Link for each Microservice
- Authentication and Authorisation Serivce -> Authentication is a process using which we can uniquely identify users in our application. This process tells us about who the user is. The general Sinup/login/logout flow is used to authenticate a user. Authorisation is a process using which, we can identify the capabilities of a user i.e. what a user can do in our application. It is more about the roles. There are various methods for Authentication such as:
    - Mobile Number - OTP or a link in mobile
    - Omniauth(gmail, fb, github) - 3rd party service is handling the authentication
    - Token Based (We use JWT - JSON Web Token in this method) - To generate the JW Token, we actually use the client credentials.
In this service, I have used Token Based Authentication for that I have used a package know as JSON Web Token.
```

https://github.com/mo-jo-dev/AuthService

```
- Booking Service -> This microservice has the functionalities of booking a tiket. While calling the API, we just need to provide our userID, flightID, number of seats we want and by these informations, we will be able to book the tickets
```

https://github.com/mo-jo-dev/AirTicketBookingService

```
