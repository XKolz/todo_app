# README
# Step-by-Step Guide
1. Set Up the Rails Project
rails new todo_app -d sqlite3
cd todo_app


2. Generate a Task Model
rails generate model Task title:string completed:boolean
rails db:migrate

3. Create a Controller for Tasks
rails generate controller Tasks

4. Define Routes
**(Open config/routes.rb and add the following line to create routes for the tasks:)**
Rails.application.routes.draw do
  resources :tasks
  root "tasks#index"  # Set the homepage to display the list of tasks
end

This will set up RESTful routes for tasks, allowing Rails to handle requests like GET /tasks, POST /tasks, etc

5. Run the Rails Server
rails server

Access the database locally
rails console
Task.all
Task.create(title: "Sample Task", completed: false)


This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
