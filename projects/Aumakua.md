---
layout: project
type: project
image: images/firstlogo.jpg
title: Welcome to 'Aumakua UH
permalink: projects/vacay
# All dates must be YYYY-MM-DD format!
date: 2018-05-09
labels:
  - Javascript
  - react-meteor-mongo
summary: My ICS 314 Final Project
---

## About 'Aumakua UH
In Hawaiian mythology, an 'aumakua is a family's guardian spirit that helps protect and guide their decsendants. Like the name, my team and I created a Meteor web application to assist incoming students in finding their scheduled classes. The instructions were to create a Meteor application that is oriented to interests of the UH Manoa community and provides personalization for a user. Reflecting on our past experiences, my team all felt that the campus map provided by the school can be somewhat difficult to use. In addition, the class locations typically shown on a student's schedule will have only the abbreviations of the buildings, leaving it up to students to manually search for each one. And so, We wanted to design an easy-to-use application that will help students with this, especially for freshman who are unfamiliar with the campus. To navigate through the University of Hawaii's large campus with Aumakua-UH, a user simply needs to add the abbreviations listed on their schedule which will generate a card with the associated route. 

More info about Aumakua-UH can be found on our page: https://aumakuauh.github.io/

## The initial phase
Working on this final project was a huge learning experience for my team, and it proved to be much more difficult that what we initially thought. The idea of a navigation tool sounded simple, but our idea didn't have a concrete structure planned out so designing a skeleton was the first step. To start off, we used a basic meteor-template to get an idea of how we wanted to separate our pages. We then decided to draw up a non-functional mockup page using images and hardcoded texts to form an outline of what we wanted the app to look like. Because we were unsure of how we would actually begin coding and how the data would be handled, we decided to just attempt it and figure it out as we progressed. 

The initial Mockup page:
![](images/mappage_initial.jpg)

### coordination
One of the most important parts of this project and my experience with it, is learning how to properly work with fellow programmers to collaborate through github. With the skeleton outlined, we decided to set aside the appearance of each page and instead focused our attention to gaining functionality. Since we wanted to form the structure for our code as we progressed, we felt it easier to break down the functionality of the project into three main parts. One was the map component that would take in data to provide a route which was tasked to Josh. The other part was the collection handling that would interact with the user and send the data to the map, and this was tasked to Keone and I. Though we divided our tasks, it was not strictly as we would regularly meet to discuss our problems and assist each other. These meetings proved very helpful for many of our problems which I will discuss further down in the next section.

For the initial part of collection handling, Keone worked on populating the database collection while I focused on interacting with the database. Working with a smaller temporary collection of sample data, I had to figure out how to pull certain properties from each element in the database to make a usable collection. Many of my attempts failed and so, I had to research further on how MongoDB collections are accessed. Through this experience, I learned how to use subscriptions and publications, and also familiarized myself with more MongoDB methods(reference linked at the bottome of this section). By the end of this, I was able to successfully make a function that will take in the abbreviation from the user, match it to an existing building in our buildings-index database and pull the data out for use. Applying similar principles, I also figured out how to populate the options for the suggested dropdown menu that Keone set up. Following which, we made a personalized user card collection for his added buildings which would automatically create a card with a submission from the dropdown menu. We then worked together with Josh to get the data from the user cards to interact with the map. 
Suggested Dropdown:
![](images/Add5_1.jpg)

Card Collection:
![](images/map5_1.jpg)

MongoDB reference: https://docs.mongodb.com/manual/reference/method/

### problems
The main problem I experienced was accessing the properties of the data pulled from the database of buildings. The data would be pulled successfully with all the properties listed, but we were unable to access any specific property. This small problem delayed our progress for 2-3 days. Eventually, we found that it was pull out the data as an array object in index 0. 
```
let bFound = BuildingsList.find((inputChoice)).fetch();
const name = bFound[0].buildingName;
    
```

## My gains
The experience I gained from this project was significant as I had no prior experience with designing a web application from scratch. I got to familiarize myself with using Meteor-react, Semantic-UI, and Mongo Database, all of which I am now comfortable using. There were also many things I would have changed if I were to redo this project. I realized after finishing, better ways to organize my code to implement more design pattersn which would have made our code cleaner and more efficient. These include separate components for accessing collections and another for the dropdown menu. I also would like to re-design the UI to be more user friendly and cleaner in appearance. This includes the delete listing options which I would make into a hidden onclick text field for submissions. Overall, I have gained valuable experience in the basics of web application design with Meteor, to which I can apply in many of my future projects.
