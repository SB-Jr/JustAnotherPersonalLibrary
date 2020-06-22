# JAPL architecture research

## Components

- UI 
  - Elements for user interaction
  - Layer to interact with engine
- Engine
  - Indexing component
  - Ranking component
  - File parsing component
  - Storage component
  - Metadata calculating component



## Requirements

### UI

The following are the requirements we are trying to achieve with the help of different tools, frameworks and libraries.

- Light weight
- Responsive
- Desktop agnostic

Given the requirements we have finalised to use the following:

- Programming Language: **Vanilla Javascript** 

  As it is one of the best cross platform UI rich language and we can achieve any given UX component easily, so choosing JS as our UI language

- Desktop Client Framework: **ElectonJS**

  This provides a easy way to create desktop interfaces and is also desktop agnostic giving us ample opportunity to experiment with better UX deigns without much hassle.

- UI testing framework: 

  A testing framework is needed to write unit test cases and scenarios to make sure we dont break any existing functionality once we have built a considerable amount of the project.

- Linting framework: 

  A linting framework to encorporate basic programing style so as to eliminate critical bugs because of poor coding habits

- UX framework: 

  A UX framwork to handle animations, user interactions and the different states in the life cycle of the application.

- Other Tools: 

  - **RequireJS**
  - Templating Library:
  - Devtron - Chrome extension specifically for electron.Handles linting. 

## Engine Requirements

These are our requirements from an ideal backend engine which will satisfy the requests of the client(UI desktop application). We will be wrapping this engine in a javascript wrapper if the chosen language is other than JS.

- Reading big files easily
- Indexing capabilities
- Storing capabilites for the calculated indexes
- Searching capabilities for a given query
- storing tags and other meta-data for each file
- Checking for updates in files and updating corresponding indexes
- providing proper feedback to UI for different tasks
- not needing extra configurations to be done by user i.e. working out of the box

GIven the following requirements we have concluded to research on the following topics:

- Programing Language: Python, JavaScript

  Python has an edge over javascript that it can easily written to handle files and reading other rich documents. It also has a variety of framework support either directly or indirectly through a wrapper.

  Javascript has an edge over python that it can be easily incorporated with our UI without much hassle. It also has nodeJs support through which we can access  multiple frameworks. 

- Indexing Engine: Elasticsearch, solr

  Indexing engine will have the task to create hash indexes for each file and then store it in the database. It should also be able to fetch the proper results when a text has been provided. 

  Plus points if it also has a built in support to rank the results.

  **Another key factor is to search for partial results** 

- Database to store indexes: 

  Key task is to be able to store and fetch results when required. Should be light weigth and work out of the box wothout much configuration or should support automated configuring which we can handle through some scripts.

- Wrapper Framework(if needed):

  A wrapper framework will be needed to provide JS APIs such that UI can easily interact with the engine.

- Tesing framework:

  To write unit test cases for the engine

- File reading Library:

  The file reading library is needed to read and parse out the actual texts from rich formats like Markdoen, HTML, LATEX, TEX, DOC, DOCX etc.

- Linting Library:

  To provide linting for better coding styles

- Ranking Library:

  If the indexing algorithm doesnt provide better ranking for the fetched results then a good ranking algorithm and its implementation is required.

  



Search through your notes/files

## **Environment**

Considering we have less UI Components to use and more backend logic, It is preferable to look into the frameworks best suited for backend logic. But we would still need to research into Frontend frameworks.

### _Possible Options for Frontend_

1. **Angular.js**  
    - Can be used to develop mobile &amp; web apps. Mobile apps with Ionic  
    - It is a full fledged framework for sw development including testing with no need of additional libraries.  
    - Learning curve is medium as it is a huge library.  
    - Performance is affected as the app becomes more complex &amp; dynamic but recent updates have improved performance data. Even the app size is lesser than the react app.  
    - App structure is fixed &amp; has MVC structure  
    - It goes well along with MEAN stack (Mongo, Express, Angular, Node)  
2. **React.js**
     - Can be used to develop mobile &amp; web apps. Mobile apps with React native  
     - It is a UI only framework providing components but needs libraries for external support like Redux for state management, stack navigation for routing.  
     - Learning curve is low due to it&#39;s minimalistic nature.  
     - Performance is good due to light-weight &amp; virtual DOM structure  
     - App structure can be flexible &amp; provides developer with freedom to experiment  

### _Possible Options for Backend_

1. **Express.js**
    - Built on top of node.js to provide middleware support to help manage our servers &amp; routes.  
    - It&#39;s robust API allows users to configure routes to send/receive requests between the front-end and the database (acting as a HTTP server framework).  
    - A good advantage with express is how it supports a lot of other packages and other template engines such as Pug, Mustache, EJS and a lot more.  
    - Focused on browsers making templating &amp; rendering easy. Supports MVC.
    - Low learning curve, lots of resources available online  

2. **Next.js**
    - Built upon front-end library React.js
    - It provides Server Side Rendering
    - It also provides the same option as React &quot;Build once, Run everywhere&quot;. It can run on Web, Mobile &amp; Desktop.
    - It offers automatic code splitting and filesystem-based routing.
    - It has built-in CSS support called CSS-In-JS
    - Also has Webpack Configurations to Continuous Deployment
    - [https://levelup.gitconnected.com/a-simple-next-js-frontend-for-a-multilingual-website-ae31a17387e2](https://levelup.gitconnected.com/a-simple-next-js-frontend-for-a-multilingual-website-ae31a17387e2)

_Factors to choose the framework:_

- Complexity of frontend - _Low_
- Complexity of backend - _High_
- Speed of the application (backend/frontend side) - _Backend fast_
- Learning curve - _Low_
- Flexibility &amp; resources available (like npm packages, libraries)

### Database:

## **Searching Algorithm/Library**

_**Elastic Search**_ as indexing and searching library

_Benefits_:

- Search analytics engine, distributed &amp; horizontally scalable
- Seamless Integration, accessed over HTTP through the RestFul API
- Enables full-text searches which indexes every line in the document

_Available as:_

NPM Package: [https://www.npmjs.com/package/elasticsearch](https://www.npmjs.com/package/elasticsearch)

_Resources:_

1. [https://www.elastic.co/guide/en/elasticsearch/client/javascript-api/current/introduction.html](https://www.elastic.co/guide/en/elasticsearch/client/javascript-api/current/introduction.html)
2. [https://www.compose.com/articles/getting-started-with-elasticsearch-and-node/](https://www.compose.com/articles/getting-started-with-elasticsearch-and-node/)