# Technical test

## Introduction

Fabien just came back from a meeting with an incubator and told them we have a platform “up and running” to monitor people's activities and control the budget for their startups !

All others developers are busy and we need you to deliver the app for tomorrow.
Some bugs are left and we need you to fix those. Don't spend to much time on it.

We need you to follow these steps to understand the app and to fix the bug : 
 - Sign up to the app
 - Create at least 2 others users on people page ( not with signup ) 
 - Edit these profiles and add aditional information 
 - Create a project
 - Input some information about the project
 - Input some activities to track your work in the good project
  
Then, see what happens in the app and fix the bug you found doing that.

## Then
Time to be creative, and efficient. Do what you think would be the best for your product under a short period.

### The goal is to fix at least 3 bugs and implement 1 quick win feature than could help us sell the platform

## Setup api

- cd api
- Run `npm i`
- Run `npm run dev`

## Setup app

- cd app
- Run `npm i`
- Run `npm run dev`

## Finally

Send us the project and answer these simple questions:

- What bugs did you find? How did you solve them and why?
  - **R/** I found 4 bugs:
    - The form to create a new user was not saving the user's name because the property name on the form was 'username' instead of 'name', which is the property name on the backend. I changed the property on the form to 'name'.
    - The search by name encountered an error when a user didn't have a name. I fixed this by making the 'name' property optional to avoid the undefined exception.
    - The form to update the user was not calling the submit function. This was because the button was using the property `onChange` instead of `onClick` (which is used for inputs). I corrected this by changing the property to `onClick`.
    - There was an error when trying to access a project. This occurred because the backend API was sending the project in a list instead of just the project itself. The solution was to change the find function on the API from `find` to `findOne`, ensuring that we will never have two projects with the same ID.

- Which feature did you develop and why?
  - **R/** I added the job title to the user search functionality because it could be useful for users to find team members with specific job titles they are looking for.

- Do you have any feedback about the code/architecture of the project and what difficulties did you encounter while working on it?
  - **R/** I think that currently, the code and architecture are fine because the application doesn't have too many features. However, as the application evolves, it might be beneficial to add more layers to the backend, such as a service layer to handle the business logic for each entity.


