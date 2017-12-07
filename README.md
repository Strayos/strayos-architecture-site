# Strayos: Architecting Sites

### Functional Specification

###### David Ayeke

Last Update: December 6, 2017

2017 Strayos, All Rights Reserved.

---

## Overview

Sites are a new way of managing and tracking user data.

This spec is not, by any stetch of the imagination, complete. All of the wording will need to be revisted several times before it is finalized. The graphics and layout of the screens is shown here merely to illustrate the underlying functionality. The actual look and feel will be developed over time with the input of graphics and iterative user feedback. 

The spec does not discuss the algorithms or implementation details, which will be discussed elsewhere. It simply discusses what the user sees when they interact with Sites and how the backend is expected to respond.

## Scenarios

In designing products, it helps to imagine a few real life stories of how actual \(stereotypical\) people would use them. We'll look at three scenarios.

#### Scenario 1: Buck Lee the Blaster. 

Buck has been hired by Old Castle Only© to design 10 blast their quarry. The customer is adamant that he is able to access all data he has, so he can share the information with his drillers. Buck decides to use Strayos. He creates an account for the Customer, and sends the login to the customer. He then flies over the bench, and uploads the data. Since Strayos doesn't recognize the location of the Flight, it prompts him to create a new Sites to collect subsequent ones. After creating the Site, he shares the Site with his personal Strayos account, and does the rest of his blast design using his own account. 

#### Scenario 2: Richard the Driller. 

Richard has been hired to drill and blast a bench on Monday. This is his fifth time drilling at the Site, and he has been given access to the Site's drill planning and inventory management. He logs onto his personal Strayos account, and sees the newest flight. He immediately goes to blast design, and runs burden analysis to ensure the blast designer didn't make any obvious mistakes. After confirming that everything looks good, he exports the shotplan in IREDES format for his smart drill. On Monday after drilling, he uploads an IREDES file his drill game him that confirms the location of the holes. He knows that Strayos can use that for fragmentaiton analysis after he flies the muck pile. Knowing the customer will chew him out if he forgets, he updates the magazine contents in the inventory management suite. 

#### Scenario 3: Detective Dave

A parking lot was just decimated by a car bomb. ATF officer Dave is going around local mines to check if any explosives could have been stolen. He was given a link to access the inventory of Old Castle Only© though the Strayos platform. He goes over all of their blast and checks how many explosives were used in each. He double checks that the seismographs and the current magazine contents match up. Failing to detect a discrepency he stops his investigatoin. 

#### Scenario 4: Chris the client

Chris is loving Strayos. Everytime his superior, Steve, wants to know how much rock was blasted this week, he can generate a pdf showing how much volume has been blasted for every single blast! He can even show a map of how the bench has changed ever since Buck started designing his blast. He was even able to deal with the ATF without worry! He's going to ask Steve for an enterprise Strayos account so that he can have the same data analysis for his quarry in Chico. 

### Goals

* Separate the people who can view \(read\), modify \(write\), and run \(execute\) the various suites in are platform.

* Associate all data with a Flight \(time\), and all flights with a Site \(location\)

* Allow the Customer to grant read, write, or execute access to any data associated with his Site. 



