# startnow-db100-mysql-exercises
startnow-db100-mysql-excerises
Introduction

In this project we're going to:
Import a prepopulated database into MySQL called sakila
Write SQL to view and query data from the database
Write SQL to insert, update and delete records in the database.
Prerequisites

Make sure you have checked off the following tasks:
[ ] Download and install MySQL Community Edition and MySQL Workbench
[ ] Read as much of this documentation as you can. It describes a prepopulated database called sakila that we will use as the basis for these SQL exercises.
[ ] Follow these instructions to load a sample database called sakila into your MySQL server.
High Level Steps

Initialize the Project
Review the Project Files
Start the first exercise
Complete the subsequent exercises
Step 1 - Initialize the Project

First, we need to perform the usual, repeatable steps to start a new project. Change directories to the project files for mysql-exercises and initialize git and npm using:
$ cd ~/oca/startnow-db100-mysql-exercises
$ git init
$ npm install
You will also need to add the following file to the root of your project - replacing the values in this file with your MySQL username/password.
config.js

module.exports = {
    username: 'your_mysql_username',
    password: 'your_mysql_password'
};
Step 2 - Review the Project Files

Next, review the files that you have been provided. You will notice we have provided 9 exercises in ./sql/exercises.sql for you to complete and a spec file containing tests. It is recommended that you use MySQL Workbench to test out your queries and visually check your work, then paste your solution in the correct .sql file followed by npm run test.
Step 3 - Start the first exercise

Open sql/exercises.sql and enter the following answers for the first three select questions:
#                              __
# .--------.--.--.-----.-----.|  |
# |        |  |  |__ --|  _  ||  |
# |__|__|__|___  |_____|__   ||__|
#          |_____|        |__|
#

# Important: Remember to add a semi-colon at the end of each query.

# ---------------------------------------------------------#

## 1. SELECT statements

# 1a. Select all columns from the actor table.
SELECT * FROM actor;

# 1b. Select only the last_name column from the actor table.
SELECT last_name FROM actor;

# 1c. Select only the following columns from the film table.
#
# COLUMN NAME           Note
# title                 Exists in film table.
# description           Exists in film table.
# rental_duration       Exists in film table.
# rental_rate           Exists in film table.
# total_rental_cost     rental_duration * rental_rate
SELECT
    title, 
    description, 
    rental_duration, 
    rental_rate, 
    rental_duration * rental_rate as total_rental_cost
FROM film;

Now, open a terminal and run the tests. The first three tests under SELECT should pass once you add the above code.
Step 4 - Complete the subsequent exercises

Now it's your turn. Utilize your resources and knowledge of SQL to complete the rest of the exercises.
Exit Criteria

All exercises should pass their associated test.
Added a README.md to the root of the project
Upload the project to GitHub
