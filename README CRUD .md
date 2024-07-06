This is a simply Web Application for REST API program using Python and Flask\
After understand how to create server from the Main directory,then this is the second step CRUD operations with Python\

I have created a Products's list using a Flask server.
This application should allow to add a product, retrieve the products, retrieve a specific product with its id, update a specific productwith its id, and delete a product with its id.\
All these operations will be achieved through the REST API endpoints in this Flask server.\

Lastly will use cURL and POSTMAN to test the implemented endpoints.\

1)Set-up : Create application using terminal first
-Open a terminal window by using the menu in the editor: Terminal > New Terminal.\
-Change to your project folder, if you are not in the project folder already. example command: cd /home/project \
- clone the Git repository that contains the starter code needed : [ ! -d 'jmgdo-microservices' ] && git clone https://github.com/ibm-developer-skills-network/jmgdo-microservices.git \
- Change to the directory jmgdo-microservices/CRUD to start working on the lab. : cd jmgdo-microservices/CRUD \
- Run the following command on the terminal to install the packages that are required. : python3 -m pip install flask flask_cors \

2) Understand the server application
- In the Files Explorer open the jmgdo-microservices/CRUD folder and view products.py. # PLease noted that in this directory I just put the product.py file only,if require the wholeprogram file please goto step 1 to cline the Git repository\
- Need to import the packages required to create REST APIs with Flask in the product.py file :
  from flask import Flask, jsonify, request
  import json
-create the Flask application, which will service all the REST APIs for adding, retrieving, updating, and deleting products.
  app = Flask("Product Server")
- After done precreated products added to the list. These are defined in the following code.
  products = [
    {'id': 143, 'name': 'Notebook', 'price': 5.49},
    {'id': 144, 'name': 'Black Marker', 'price': 1.99}
]
- Now that the server is defined, we will create the REST API endpoints and define the routes or paths, one for each of the following operations.
  -Retrieve all the products - GET Request Method
  -Retrieve a product by its id - GET Request Method
  -Add a product - POST Request Method
  -Update a product by its id - PUT Request Method
  -Delete a product by its id - DELETE Request Method
  # You may find this in the product.py file

3) Run and test the server with cURL
-In the terminal, run the python server using the following command.
  python3 products.py
-Open another Terminal by clicking the Terminal menu and selecting New Terminal.

# In the new terminal, run the following command to access the http://localhost:5000/products API endpoint. curl command stands for Client URL and is used as command line interfacing with the server serving REST API endpoints. It is, by default, a GET request.
  curl http://localhost:5000/products
  
-In the terminal, run the following command to add a product to the list. This will be a POST request to which you will pass the product parameter as a JSON.
  curl -X POST -H "Content-Type: application/json" \
    -d '{"id": 145, "name": "Pen", "price": 2.5}' \
    http://localhost:5000/products
    
-Verify if the product is added by running the following command.
  curl http://localhost:5000/products/145

-Last While the GET endpoints are easy to test with curl using a command line interface, the POST, PUT and DELETE commands can be cumbersome. To circumvent this problem, you can use Postman, which is a software that is available as a service.

You may try it throught the Postman Software

Example code used in Postman
-Paste the URL that you have copied into the address bar. Change the request type to POST. To send input as JSON, choose raw->body->JSON.
-Enter the following JSON object and click the Send button. This will add the product to your previous list of products.
  {
      "id":146,
      "name":"Laptop Bag",
      "price":45.00
  }
-Verify the list of products to ensure that the request has gone through and the product is added. Change the request type to GET and remove the JSON object from the request body. Click Send and observe the output in the response window
-Test the PUT endpoint to update product details by changing the price of the item with id 146 to 42.00. Set the request type to PUT and add the product id to the end of the URL and add the value to be changed as a JSON body and click Send.
  {
      "price":42.00
  }
-Verify the product with id 146 to ensure that the request has gone through and the product is updated. Change the request type to GET and remove the JSON object from the request body. Click Send and observe the output in the response window.
-Go to products/144 endpoint. Set the request type to `PUT` and add the product id to the end of the URL and add the value to be changed as a JSON body and click `Send`.
-Go to products/142 endpoint. Set the request type to `DELETE` and click `Send`.
