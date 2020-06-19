<p align="center">
  <img width="200" height="200" src="https://media-exp1.licdn.com/dms/image/C4E03AQFr1viytj_VQA/profile-displayphoto-shrink_200_200/0?e=1597881600&v=beta&t=5PTBuTdNqtTcUbtcfeRLDowPjvtODnUS1q7lS8NrY4g">
</p>

<h3 align="center">Bijan's Portfolio</h3>

<p align="center">
  Hello world, thanks for stoping by my personal Github.
  <br>
  Below you'll find background on myself and the projects I have worked on over the years.
</p>

## Table of Contents 

- [AEG](#aeg)
- [EY](#ey)
- [NFL](#nfl)

## AEG: Ticketing Application
AEG is one of the largest companies in the live entertainment industry, they book shows at venues and generate revenue from ticket sales. 

The objectives of the AEG Ticketing Application are to first ingest ticket sale data from 3rd parties then associate it with events created in external booking applications.

Below are several features which I enjoyed implementating for this application

#### Ticket Sales ETL 
![screenshot](assets/img/Presentation2.jpg)
Everytime tickets are sold for an AEG show raw ticket sale data from 3rd parties is sent to AEG's datawarehouse.

The raw data is then available for the Ticketing Application to ingest, upon import the raw data is transformed to the intermediate ```ticket_feed_wrap``` table.

The ```ticket_feed_wrap``` tables are then transformed and split into their target tables ```ticket_events``` and ```daily_counts```. 

I was responsible for defining the tables required at each step of the transformation, along with testing the outcome of the Ticket Sales ETL. 

See documentation below for details: 

[Ticketing ETL Product Requirements](https://github.com/bayrami1/work-experience-/blob/master/AEG%20Project/ETL%20Product%20Requirements%20.pdf)

#### Matching Ticket Events to Events in different applications
Everytime a ticket sale is imported into the Ticketing App BE new ```ticket_events``` and ```daily_counts``` objects are created, these tables represent the ticket sales associated with a given show or ```booking_events``` created in AEGs booking applications.   

The second objective of the Ticketing Application is too associate ```ticket_events``` with ```booking_events```, for reporting and forecasting. 

(include reworked ppt and remove microservice) 

To accomplish this a second ETL pipeline was created to import ```booking_events``` from different applications store them on the Ticketing BE and then create an workflow that would allow users to use an interface to make the association between the events. 

The first step required standardizing the ```booking_events``` created in other systems and import them into our backend, which is covered in the documentation below: 

[Booking Events Import](https://github.com/bayrami1/work-experience-/blob/master/AEG%20Project/TA%20_%20booking_events%20creation%20.pdf)

The second step required creating an intuitive workflow that would allow users to easily make the association between Ticket Events and Booking Events (NOTE: there are no recommended booking events for the given ticket events in the screenshot above because we were using test data) 

What made this feature so exciting was the need to have a deep understanding of the data and technical requirements but also required working with design to make sure once all the data was in the right place we had the appropriate UX in place so that business goals were accomplished. I worked very closely with the data team at AEG to make sure the ETL went smoothly and also working with design to make sure that we had the appropriate UX in place.  

#### Access Control and Privacy Settings
Talk about how it took a lot of user interviews and because it directly impacted business it had to be approved by key stakeholders and product council. 

## EY
#### Storage Manager 
Due to the proprietary data for this project I am unable to share documentation or architecture relating to the project 
- created SM, which was created to manage very sensitive Tax data 
- accomplished using a proprietary cloud agnostic architecture using multiple services 
- created the Tax application which used tokens generated by the storage manager to access sensitive data and automate tax pipelines which were done manually in the past
- the creation of the storage manager and the automated pipelines ran through the tax application allowed the Tax team to increase efficiency of their team by 25%

## NFL 
#### Fantasy Football Data Analysis Project
