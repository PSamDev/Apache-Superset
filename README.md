# Apache-Superset
Apache Superset is a data visualization tool used to display data in chart or graphs

# Installation 
Create a virtual environment *python3 -m venv venv* 
Activate virtual environment *venv/bin/activate*
Download latest version of pip and setuptools *pip install --upgrade setuptools pip* 

# Install superset
pip install apache-superset

# Create a superset_config.py inside the site_packages folder on the lib section of your virtual environment

# Generate a secret key 
openssl rand -base64 42

# Create a variable named SECRET_KEY inside the superset_config.py file your created and input yout secret key as a string
SECRET_KEY = "Your generated secret key"

# Initialize the database
superset db upgrade

# You will be prompted to set a username, first and last name before setting a password (Add Admin User details)

# Set superset as flask app
$ export FLASK_APP=superset
superset fab create-admin

# Load some data to play with
superset load_examples

# Create default roles and permissions
superset init

# Start a development environment 
superset run -p 8088 

# Login with your admin Details 
