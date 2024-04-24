# ASL_For_Everyone
Summer ASL translator project

## Running the App

### Requirements to run the app
1. Python 3.6 or above
2. Node 16 or above

Make a copy of the `.env.sample` files present in the `server` folder and name it as `.env`.
Replace the content with your appropriate values.
The `.env` file in the `server` folder will contain the database url and the secret key for the JWT token. The secret key for the JWT token can be left unchanged for development purposes, but the database url will need to be changed. Instructions for creating a database url with MongoDB Cloud be are given below. You may also need to change the `FLASK_HOST` key to be `0.0.0.0` if you are running the mobile app on a physical device on the same network. 


### Instructions to run the app
Depending on your Python install, you may need to use `python3` and `pip3` instead of `python` and `pip` respectively.

1. To run the Flask server: \
    Change directory to the server folder: `cd server` \
    Create a venv in the server folder: `python -m venv venv` \
    Activate the virtual environment \
    Install the dependencies: `pip install -r requirements.txt` \
    Run the server: `python app.py`

2. To run the ReactJS client: \
    Change directory to the client folder: `cd web` and `cd main_app` \
    Install the dependencies: `npm i` \
    Run the application: `npm start`


### Making a Cloud MongoDB database
1. Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) and create an account.
2. Create a new project and a new cluster.
3. Create a new database named whatever you want.
4. Click on the connect button and select the appropriate options. (Note: when replacing `<password>`, make sure to use your user password and not your account password)
5. Copy the connection string and paste it into the `MONGO_URI` key in the `.env` file in the `server` folder.
6. Set the `MONGO_DB_NAME` in the `.env` file in the `server` folder to the name of the database you created in step 3.
