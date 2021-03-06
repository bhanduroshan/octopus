# Tornado Word Cloud App #

This demo is a simple word cloud demo app that uses encoding algorithm to encode words and store words in database.
You must have MySQL installed to run this demo.

## One line command to run:  docker-compose up ##
- If you have `docker` and `docker-compose` installed, the demo and all its prerequisites can be installed with `docker-compose up`.

## If you dont have docker-compose, Please follow following steps: ##
- Install mysql database if needed
- Install Python prerequisites
   This demo requires Python 3.5 or newer, and the packages listed in
   requirements.txt. Install them with `pip -r requirements.txt`
- Create a database and user for the blog.
   Connect to the database with `mysql -U root -p` (for Mysq;)

   Create a database and user, and grant permissions:
   
      1. mysql -u root -p
      2. Create database octopuslabs;
      3. CREATE USER 'octopus'@'localhost' IDENTIFIED BY 'octopus123';
      4. use octopuslabs;
      5. GRANT ALL PRIVILEGES ON octopuslabs.* TO 'octopus'@'localhost';
 - Run the code -- Python manage.py Runserver

## Architecture ##
- Follows MVC pattern
- Models.py: Define database table, also has manager to run crude operation on top of model
- urls.py - file used to route request
- views.py - file that has logics stored for request, i.e Handlers
- Other Files:
  - static: fodler that contains static files
  - templates: folder that contains templates that are rendered
  - utility: contais files that do encryption, decryption, wordcount etc

## Using the App ## 
- Visit y -- http://localhost:8888 in your web browser.
- Enter a url to get word cloud
- Once you get word cloud, visit -- http://localhost:8888/admin
- You will need to login, if not logged in, use following credentials
   - * user: octopus 
   - * passwrod: octopus123
- You will then be redirected to admin page
