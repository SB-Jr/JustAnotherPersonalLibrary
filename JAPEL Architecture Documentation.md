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