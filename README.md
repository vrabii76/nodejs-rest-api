# REST API using Node.js and Express

This RESTful API have:

1. A '/products' resource that supports following requests:
   GET - get all products
   POST - add new product
   Also I'm able to access the individual product by id and
   get information about that product with following requests:
   GET - get a single product by id
   PATCH - update product information
   DELETE - delete product

2. A '/orders' resource that supports following requests:
   GET - get all orders
   POST - create a new order
   Also I'm able to access the individual order by id and
   get information about that order with following requests:
   GET - get a single order by id
   DELETE - delete order

3. A '/user' resource that supports following requests:
   POST using 'user/signup' route - to sign up user
   POST using 'user/login' route - to login user
   DELETE - delete user by id

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
