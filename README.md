## Installing required Packages:

First install the packages required for the application.

    pip install -r requirements.txt
(or)

    pip install fastapi psycopg2-binary uvicorn python-dotenv python-multipart
        
Note: make sure on python-dotenv not dotenv

## Understand before running the file:
    
This file can run on git codespaces as well as render free hosting website. The python file runs on uvicorn server for hosting purpose. 

If you want run on your local machine, then remove the if condition which declared the uvicorn server to run as app.

### Environment file:
    
.env file is used in this application to maintain the hostname, port, username, password and database credentials.

I have used in the python file by importing dotenv package of load_dotenv and it is used in main method which loads on loading of the file.
    
Using os package, accessing environment variables by using os.getenv("env_var") method.

### Connectivity:
    
In this application, we use fastapi with posgresSQL which is hosted from render hosting websites.

### Functionality:
    
In this application, we connected posgresSQL with fastapi to return response to ReactUI which store and get data from imagess table in database.

We are uploading an image file from ReactUI which received in fastapi and store it in posgresSQL in imagess table.

And retrieval of image in response from same imagess table which will be available in response only, not integrated in UI. Use developer tool and see the image.
    
Added CORS, to run in any environment.
    
We can test it without UI also by running the url and add /docs#/ at the end to get Swagger documentation and run the apis to test.
