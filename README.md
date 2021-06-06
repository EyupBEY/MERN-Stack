# MERN-Stack
This repo was made using a video on the freecodecamp youtube channel (https://www.youtube.com/watch?v=mrHNSanmqQ4&amp;list=PLdRnihRBaZHQc0ZD0TOh6t8RXhbo-LNV9&amp;index=3).

1- Open Mongodb new project
2- Create a new cluster
3- Connect ---> Add this ip address ------> Create db user ------> Choose connection method -----> Connect your application ---->(copy the thing nearly similar to mongodb+srv://<username>:<password>@cluster0.341fn.mongodb.net/myFirstDatabase?retryWrites=true&w=majority) -----> Close
  
4- (...) Load sample db    -wait for a while-
5- Collections

  
Terminal:
  /Desktop$ mkdir mernstackproject
	$ cd mernstackproject
	$ mkdir backend
	$ cd backend
	$ npm init -y	(init sanırım initiated in kısaltması)
	$ npm install express mongodb cors dotenv 
    (CrossOriginResourceSharing) allows ajax requests to skip the same origin policy and access resources from remote hosts. It provides express middleware that can enable cors with different options. We can make the right connections on our network that we need to make without that we could have some errors.
    (mongodb) allows us to interact with the mongodb database.
    (dotenv) loads environmental variables from a .env file in the process.env . So this makes development simpler.

  $ npm install -g nodemon
	  (nodemon) makes development easier. It helps develop node.js based applications by automatically restarting the node application when file changes in the directory are detected. So we don’t have to restart the server when we make an update.
  
  $nodemon index.js
  
  
  .env file'a RESTREVIEWS_DB_URI=mongodb+srv://EyupBEY:abrakadabra4563271615LBCE+@cluster0.341fn.mongodb.net/sample_restaurants?retryWrites=true&w=majority yazdık, 3 yer değiştirdik.
  
 ------------ Code whole backend/ ------------
 
  By the way, you can use **a browser or Insomnia or Postman **to GET requests.(http://localhost:5000/api/v1/restaurants  , http://localhost:5000/api/v1/restaurants?zipcode=11224)

  MongoDB
    Collections ----> Sample Restaurants ----> restaurants ------> Create Index ------> {"name":"text"} ----> Review -----> Confirm
      The alternate way to do this open Insomnia POST http://localhost:5000/api/v1/restaurants/review   Body ----> Json
        {
          "restaurant_id": "idThatICopiedFromGETrequest",
          "text": "Great food!",
          "user_id": "1234",
          "name": "blah"
        }
        Send
  
      To find it on MongoDB:
        Collections(refresh the page) ----> Sample Restaurants ----> Reviews
  
  $ cd ..
	$ npx create-react-app frontend
  $ npm install bootstrap
  $ npm install react-router-dom
