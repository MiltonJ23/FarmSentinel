# FarmSentinel 🌾 : Cloud-based monitoring and alerting platform for real-time, geolocated crop health, pest and diseases reports.


---

**FarmSentinel** is a cloud-based web application , allowing the farmers to register and mark their fields , their area on a map; log crops variety ,  yields and reports pest and disease incident. Reports are geotagged and streamed in real-time , so nearby farmers and authorities see evolving outbreaks on the map , receive alerts and can make mitigations decisions by then. 


To grasp this software project , we are going to describe the problem , outline the problem scope , then , delve into the solution proposal based on distributed systems , leading us to the solution's system design,then make a proposal of technologies to implement the system and finally, present a calendar of activities.


---

## Table of Contents 

1. [Problem Description](#1--problem-description)
2. [Problem Scope](#2--problem-scope)
    * [Clear Problem Statement](#clear-problem-statement)
    * [Project Boundaries](#project-boundaries)
        * [Functionality and features](#functionalities-and-features)
        * [Target users](#target-users)
    * [Constraints  ](#constraints)
        * [Time and resources](#time-and-resources)
        * [Technical Constraints](#technical-constraints)
3. [Solution proposal ](#3--solution-proposal)
4. [System Design](#4--system-design)
5. [Technology stack](#5--technology-stack)
6. [Calendar of activities](#6--calendar-of-activities)
7. [License](#7--license)
8. [References](#8--references)

---

## Problem Description 🔎

My favorite breakfast, BHB(Beignet-Haricot-Bouillie), as for many cameroonians, is anything but a one-bite wonder. A meal consumed each day across the territory; however, its constituting elements(wheat, beans, maize, you name it) poorly come from local production,  as smallholder local farms cannot sustain the demands. As for many other crops, the yield gap, the difference between the potential agricultural yield in ideal conditions and the actual yields farmers harvest, is too large in sub-saharan africa ( [Van Ittersum et al,2013](https://www.sciencedirect.com/science/article/pii/S037842901200295X) ).

During its research to standardize yield gap assessment, agriculture scientist Martin Van Ittersum found many reasons for the yields gap in sub-saharan africa as : Water & nutrients factor(limiting factor) , weeds , polluants, pests and diseases(reducing factor) ( [Van Ittersum et al,2016](https://doi.org/10.1073/pnas.1610359113)). 

Well addressing the abovementioned issues can reduce the yield gap, thus increasing the food output of smallholder famrs and contribute to shrink food instabilitiy in Cameroon in particular, and, in the sub-saharan region in general. 

This project addresses the challenge of leveraging distributed systems and cloud computing technologies to mitigate the pest and diseases factors to reduce yield gap.



## Problem Scope 🌐 

   
 ### Problem Statement ✍🏾

 After describing the problem, this project aims to solve __the lack of systematical awareness mechanisms(`monitoring & alerting`) across farmers to reduce the impact of pests & diseases on crops yield in sub-saharan africa__.


### Project Boundaries 🌍 

The project is going to be geographically conscripted to `Cameroon`'s national territory 🇨🇲 and its farmers.

#### Functionality and Features 🪢

`FarmSentinel` is going to allow farmers to be reports pests and diseases outbreaks and be notified about incoming ones in order to take the mitigations measures. Moreover it is going to allow authorities to monitor pests and diseases outbreaks evolution in real-time and allow them to make data driven decisions. 

The features of `FarmSentinel` are as follows:

* allows farmers authentication on the platform
* allows farmers to mark their fields with precise geographical coordinates 
* allows farmers to log the area of cultivation, crops variety and yields estimations 
* allows decision-makers to authenticate on the platform in order to monitor outbreaks evolution
* allows a dedicated admin interface to manage administration's accounts
* allows the monitoring of the pests and diseases outbreaks on an interactive map 
* allows a priority ranking of outbreaks

#### Target Users 👨🏾‍🌾👨🏾‍⚖️

After defining the functionality and features of the solution, let's identify the the primary users that are going to interact with our solution. 

The users that are going to interact with our solution are: 

* `Farmers` 👨🏾‍🌾 
* `Decision makers` 👨🏾‍⚖️

### Constraints and dependencies 🧶 

#### Time and resources constraints ⏳ 

The implementation of the solutions is occuring during the `Distributed Systems and Cloud Computing` course and needs to be complete before the end of the semester; leaving with a timeframe of approximately `3 months` of execution. 

The solution will be deployed using `on premises` cloud computing resources, in our case, it will be deployed on 3 `VPS`(Virtual Private Server).

Given this solution will be `distributed systems and cloud computing ` oriented, the `computing intensive` aspect of the project should be emphasized. 


#### Technical Constraints 🔩 

A `distributed system` orientation, means the solution should be `Scalable`, `Fault Tolerant` and allow `Collaboration`. The details on those aspects of the system are going to be further discussed in the `Solution Proposal` Section. 

The system should allow real-time implementation and concurrent executions. 
The system is also going to manage `geospatial` informations and manage an `interactive map`.

The map navigation should have the lowest latency possible for a pleasant user experience. 

Moreover,in order to make the system more reliable,  the communication between some services will be `asynchronous`, thus involving the use of `message broker`.



## Solution Proposal 🚀  

`FarmSentinel` is a cloud-based web application, that is going to aggregate the farmers's data, data about their farms(geoposition, area, crops variety, yield estimation) and data on pests & diseases outbreaks(Signaling date, type, images, fallouts,etc.). 

Once an outbreak is registered, it will be displayed on the interactive map by a color code -depending on the severity of the outbreak- using the report location; Nearby farmers are going to be notified about the outbreak, thus allowing them to take respective mitigation measures.

The interactive map will display the evolution of the outbreaks in real-time  to decision-makers, in order for to make data driven decisions. 

While dealing with an outbreak, decision-makers will have to rights to modify the severity level of an ongoing outbreak and mark them done.

The non-functional requirements of the system are : `scalability`, `performance` and `reliability`. This means, we should make sure that :

- First, the system should be able to perform and operates well as the number of users or requets increases.
- Second, the system should be able to achieves its timing requirements using the available resources.
- Finally, the platform must be reliable to notify consistently about outbreaks and display the real-time evolution of outbreaks


To address our requirements (`functional & nun-functional`), we will proceed with an hybrid architecture, comprises of  `microservices` architecture and `event-driven` architecture. 


After presenting the solution, let's explore the `distributed systems` characteristics of the solution. 


### Scalability

Leveraging the microservices architecture will ensure the system is divided into single computation, self-reliant, units (services). 

This configuration will allow to increase services's instances to automatically meets the load, and decrease accordingly to adapt to the load. 

### Fault tolerant

Againg leveraging microservices, we are going to deploy and replicate microservices accross the production environment of 3 geographically disperse VMs all working in a Virtual Private Cloud network. 

The replication of the services on the VMs will ensure the system's ability to achieve its requirements even if a part of the system is down. 


### Collaboration 

The platform will allow logged in decision makers to edit the severity of outbreaks. 




## System Design 


This section is going to provide an in-depth understanding of the system using diagrams .









## Tech stack 

I will proceed with NextJs & Mapbox Gl for frontend, because of the map functionalities of mapbox gl and next for the way it handles components, it is modern. I will go with golang for the backend because it is easier to set concurrency with it and also because it is the language of most of modern distributed systems . For the database, since i am dealing with structured data and i will need to deal with geospatial data, i will go with postgres and postgis . I will use a self hosted minio for object storage and rabbitmq for message queueing 



