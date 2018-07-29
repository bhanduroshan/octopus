Running the Tornado Word Cloud Demo

This demo is a simple word cloud demo app that uses encoding algorithm to encode words and store words in database.
You must have MySQL installed to run this demo.

If you have `docker` and `docker-compose` installed, the demo and all
its prerequisites can be installed with `docker-compose up`.

1. Install mysql database if needed
2. Install Python prerequisites

   This demo requires Python 3.5 or newer, and the packages listed in
   requirements.txt. Install them with `pip -r requirements.txt`

3. Create a database and user for the blog.

   Connect to the database with `mysql -U root -p` (for Mysq;) or
   `cockroach sql` (for CockroachDB).

   Create a database and user, and grant permissions:

      1. mysql -u root -p
      2. Create database octopuslabs;
      3. CREATE USER 'octopus'@'localhost' IDENTIFIED BY 'octopus123';
      4. use octopuslabs;
      5. GRANT ALL PRIVILEGES ON octopuslabs.* TO 'octopus'@'localhost';

5. Run the code -- Python manage.py Runserver
6. Visit y -- http://localhost:8888 in your web browser.
7. Enter a url to get word cloud
8. Once you get word cloud, visit -- http://localhost:8888/admin
9. You will need to login, if not loggedin use user- octopus and passwrod - octopus123
10.You will then be redirected to admin page