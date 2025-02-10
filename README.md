# REST API using Node.js and Express

This RESTful API have:

1. A '/products' resource that supports following requests:<br/>
   GET - get all products<br/>
   POST - add new product<br/>
   Also I'm able to access the individual product by id and<br/>
   get information about that product with following requests:<br/>
   GET - get a single product by id<br/>
   PATCH - update product information<br/>
   DELETE - delete product<br/>

2. A '/orders' resource that supports following requests:<br/>
   GET - get all orders<br/>
   POST - create a new order<br/>
   Also I'm able to access the individual order by id and<br/>
   get information about that order with following requests:<br/>
   GET - get a single order by id<br/>
   DELETE - delete order<br/>

3. A '/user' resource that supports following requests:<br/>
   POST using 'user/signup' route - to sign up user<br/>
   POST using 'user/login' route - to login user<br/>
   DELETE - delete user by id<br/>

Users resource represents authentication functionality and
was implemented to make sure that some of these routes/endpoints
are protected so that only logged in users can access them.

Handling CORS to allow other clients to access API.

Added MongoDB database and connected products and orders routes via Mongoose.
Using Mongoose validation to ensure that only the right data makes it into the database.

Added authentication functionality, users can sign up and sign in and certain
routes are only accessible by authenticated users.
A JSON Web Token is generated after a successful login.

API also supports uploading an image when creating a new product. For that I'm using
Multer middleware which is primarily used for uploading files.

Using controllers (MVC pattern) to manage routes logic.
