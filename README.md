# EJS-digitalocean-tutorial-ddang4


> CSCI-6655-02 Web database Appl Development EJS Task
> How To Use EJS to Template Your Node Application

## Prerequisites
- A local development environment for Node.js.
- This tutorial was originally written for express v4.17.1 and ejs v3.1.5. 
- It has been verified with Node v16.0.0, npm v7.11.1, express v4.17.1, and ejs v3.1.6.

## Setting Up the Project
> 1. First, Open your terminal window and create a new project directory.
> 2. Intialize a new npm project
> 3. Install the express package
> 4. Install ejs package.

## Step-1 Configuring with server.js 
> With all of the dependencies installed, let’s configure the application to use EJS and set up the routes for the Index page and the About page. For that create a new server.js file 
> This code defines the application and listens to port **8080**.

## Step-2 Creating the EJS Partials
> Partials is the code that is reused. In this example, there will be three partials that will be reused on the Index page and About page: head.ejs, header.ejs, and footer.ejs. 
> Create a new **views** directory and then create a new **partials** subdirectory.
> In the partials subdirectory, create **head.ejs** (which has metadata for the head for an HTML document), **header.ejs** (contains about the navigation for an HTML document and uses several classes from Bootstrap for styling), and **footer.ejs** (contains copyright information) files.

## Step-3 Adding the EJS Partials to Views

> Till now we have 3 partials defined. Now we can include them in the views.
> Create **pages** subdirectory in the **views** directory. 
> In this create **index.ejs** file and **about.ejs** file (adds a Bootstrap sidebar to demonstrate how partials can be structured to reuse across different templates and pages).
> Use <%- include('RELATIVE/PATH/TO/FILE') %> to embed an EJS partial in another file.

>> The hyphen <%- instead of just <% to tell EJS to render raw HTML.
>> The path to the partial is relative to the current file.

## Step-4 Passing Data to Views and Partials

> We need to define basic variables and a list to pass to the index page
> In the **server.ejs** defines an array called mascots and a string called tagline
> We use <%= tagline %> to echo a single variable which we used in index.ejs file.
> We use .forEach for looping over the data in index.ejs.

> To run the application start the server, when the server is listening visit **http://localhost:8080/** in a web browser.


