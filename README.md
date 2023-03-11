## connection with flask and mongodb
    client = MongoClient('localhost', 27017) 
    db = client.API # create table
    myapis = db.apis # triger

## create simple page and  route for all CRUD Function
```
   @app.post('/')
    def Home():
        return "Home page
```
## Home Page ( GET ):
    - use find method and add into list and itret the _id
    - get return the response with payload of data

## Add User  ( POST ):
    - set a variable with a key and value
    - use ```insert_one```  method 
    - return response 

## Update User  ( PATCH ):
    - get id using rout and pass in function 
    - use ```update_one```  method 
    - pass two argument 1) id and 2) what update you nedd
    - return response 

## Delete User  ( DELETE ):
    - get id using rout and pass in function 
    - use delete_one method 
    - pass one argument : id 
    - return response 


## for error and response method :
```
@app.errorhandler(404)
def error404(error=None):
    Message = Response(response=json.dumps(
        {
        'Status':404,
        'Message':'Page Not Found '
        }),
        status=400)
    print("******  Error  *******")
    return Message




 
