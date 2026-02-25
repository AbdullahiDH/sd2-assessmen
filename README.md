Week 2 – HTML Forms (GET and POST)
This week I made two HTML forms — one using GET and one using POST — and tested them with httpbin.org to see the difference between how they send data. I also styled them using Milligram CSS.

What I did
Made form-get.html that sends form data using GET. The data shows up in the URL and in the args section on httpbin.

Made form-post.html that sends form data using POST. The data is sent in the request body and shows in the form section on httpbin.

Added Milligram, Normalize.css, and Google Fonts to make the forms look better.

Used Chrome DevTools to check what was being sent and took screenshots to compare the two methods.

Difference between GET and POST
GET: puts the data in the URL, so it’s visible in the address bar and can be bookmarked or shared.

POST: sends the data in the background, so it’s not shown in the address bar.

On httpbin, GET data is under "args", POST data is under "form".

Week 3 – Docker, MySQL and phpMyAdmin

This week I containerised my Node.js web application using Docker and Docker Compose. I created a multi-container setup including a web service, a MySQL database, and phpMyAdmin for managing the database.

What I did

Created a docker-compose.yml file to define three services:

Web service – Runs the Node.js application on port 3000.
Database service – Uses the MySQL image and runs on port 3308.
phpMyAdmin – Runs on port 8081 to manage the database through a browser.

I used an .env file to store environment variables such as:

MYSQL_USER

MYSQL_PASSWORD

MYSQL_ROOT_PASSWORD

MYSQL_DATABASE

This keeps sensitive information outside the main code.

The web container connects to the database container using Docker networking. The database data is stored using Docker volumes so the data persists even if the container is restarted.

phpMyAdmin

I installed phpMyAdmin using the official Docker image. It connects to the MySQL container and allows me to view databases, tables and run SQL queries in the browser.

phpMyAdmin runs at:
http://localhost:8081

Database

The database container uses the MySQL image.
Database name: sd2-db

The connection details are configured using the .env file and linked through docker-compose.

How to run

Make sure Docker Desktop is running.

In the project folder run:

docker-compose up --build

Then open:
Web app → http://localhost:3000

phpMyAdmin → http://localhost:8081

This setup creates a complete development environment using containers.

