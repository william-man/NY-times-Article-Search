## Project Description

The New York Times Articles search APP is a web app that allows the user to search and request articles published by the New York times using the developer API.

To view a demo : [Link](https://new-york-times-api-project.herokuapp.com/)

### Briefing

The requirements this project must satisfy are:

1. Home page displays the daily top articles published in the New York Times from all sections.
2. The user must be able to read a snippet of the article and a link must be provided to the source.
3. There must be a seperate page for searching for articles and a page for filtering for the top 15 books by category.
4. The page for searching for articles must provide a search bar for users to search about a keyword.
5. The page for filtering books by category must have a drop-down list to allow users to select a category they're interested in.


### Challenges

This project was originally intended to help me get more comfortable working with React but I wanted to try adding JSX into a project. This lead to a few problems during development and deployment.

The problems I needed to deal with are:

1.  `require()` not defined on the browser/client-side javascript.
2. API key not revealed in the browser.
3. Deployment on heroku.

To solve the first problem, I needed to find a way to enable `require()` on the browser so I decided to use webpack which generates a bundle by mapping all dependencies my project needs. At the same time, since JSX is not supported in browsers, webpack allowed me to create a configuration file to use babel and compile JSX into backwards compatible javascript for older browsers.

For the second problem, to hide the api key, I decided to have the server handle the search requests and then send the results forward to the client so that the key will not be revealed in the browser. To do this, I used the Express framework to help me handle the routes and requests for the app as well as to deploy the project on heroku.

### Improvements
