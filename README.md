# Property Management System API

This is a Property Management System API that allows you to manage landlords, properties, and tenants.

## Learning Goals

- Build a web basic API with Sinatra and Active Record to support a React
  frontend

## Introduction

The focus of this project is **building a Sinatra API backend** that uses
**Active Record** to access and persist data in a database, which will be used
by a separate **React frontend** that interacts with the database via the API.

## Requirements

For this project, you must:

- Use Active Record to interact with a database.
- Have at least two models with a one-to-many relationship.
- At a minimum, set up the following API routes in Sinatra:
  - create and read actions for both models
  - full CRUD capability for one of the models: 
  The update action should be implemented using a form that is 
  pre-filled with existing values for the object. On submission of 
  the form, the object should update. Note: Using a like button or 
  similar will not meet the update requirement.
- Build a separate React frontend application that interacts with the API to
  perform CRUD actions.
- Implement proper front end state management. You should be updating state using a
  setState function after receiving your response from a POST, PATCH, or DELETE 
  request. You should NOT be relying on a GET request to update state. 
- Use good OO design patterns. You should have separate classes for each of your
  models, and create instance and class methods as necessary. 
- Routes in your application (both client side and back end) should follow RESTful
  conventions.
- Use your back end optimally. Pass JSON for related associations to the front 
  end from the back end. You should use active record methods in your controller to grab
  the needed data from your database and provide as JSON to the front end. You
  should NOT be relying on filtering front end state or a separate fetch request to
  retrieve related data.

  ## Entity Relational Diagram

![project](https://user-images.githubusercontent.com/99965020/222998077-1332ebeb-4f73-43c9-8460-ad41d2d27687.png)


## APi Endpoints

The following API endpoints are available:

### get all landlords
  get "/landlords"
    
  ### get all properties
  get "/properties"
   
  ### get a properties
  get "/properties/:id"
    
  ### get property count
  get "/total properties" 
    
  ### get active users
  get "/active tenants"
    
  ### get monthly rent
  get "/month rent"
    
  ### get all tenants
  get "/tenants"
    
  ### creating property
  post "/property" 

  ### creating tenant
  post "/tenant"

  ### patch tenant requests
  patch "/tenant/:id"

  # updating property
  patch "/properties/:id"

  ### delete tenant 
  delete "/tenant/:id" 

  ### delete property
  delete "/property/:id"


  ## Installation

 1. Clone the repository
  ``git clone https://github.com/<username>/phase3-project-backend-api.git`
`

2. Install the dependencies
`bundle install`

3. Run the migrations.
`bundle exec rake db:migrate`

4. Seed the database.
`bundle exec rake db:seed`

5. Start the server
`bundle exec rake server`

6. Open your browser and go to http://localhost:9292/ to verify that the API is working.

## Deployment
[https://phase-3-project-backend-production.up.railway.app/]