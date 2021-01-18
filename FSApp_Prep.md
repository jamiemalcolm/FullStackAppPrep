## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?

A. the routes are defined in the create_router.js file and exported to server.js which adds the prefix


2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

A. Client is responsible for the logic in the app, it creates the front end 

  the server hosts the back end and links into the database

3. What are the the responsibilities of server.js?

A.  server.js sets up the localhost server adn the mongodb database

4. What are the responsibilities of the `gamesRouter`?

A.  gamesRouter is where the crud methods are defined and these could in theory be used by other applications with a similar data structure

5. What process does the the client (front-end) use to communicate with the server?

A. the client imports the GamesService.js which links in the server and database to the app so it knows where to use the crud methods ??

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs


A.  the fetch() method can take an init object which may include the method("POST", "GET" ect)

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

A.  it consumes the baseURL defined in gameService.js which is '/api/games/' and '/api/games/id:'

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

A. it allows us to comunicate from our frontend to the db?


## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
