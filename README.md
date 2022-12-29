# Basic-Website-Social-Media-Format-

Creating a simple social media that allows users to create an account and post messages that other people can read. 

Entitity Relationship Diagram (ERD) was used to create the database design strucuture. 

I used MySQL command prompt, to grant only one user access to the database (for extra protection). 

#Code used 
CREATE DATABASE friendzone;

GRANT ALL ON _.*TO '_'@'localhost'
IdENTIFIED BY '_';


Functions.php is the file that is included by the other files. Only a single require_once is needed in each file. 

Header.php starts by calling the function session_start, this set up a session that will remember certain values I want to store across different PHP files. In conclusion, it represents a visit by a user to the site, and it can time out if the user ignores the site for a long period of time. 

With the session started, the program then outputs the HTML needed to set up each web page, including loading stylesheets and the various JavaScript libraries required. After this the file of functions (functions.php) is included, and the default string of ‘Welcome Guest’ is assigned to $userstr. 

Next the code checks whether the session variable user is currently assigned a value. If so, a user has already logged in, so the variable $loggedin is set to TRUE and the username is retrieved from the session variable user into the PH variable $user, with $userstr updated appropriately. However, if the user has not yet logged in, then $loggedin is set to FALSE. After all it, some HTML is output welcoming the user (or guest if not yet logged in). 

Password checks would be done both on the front end, and on the back end to ensure consistency. Front end check will force users to set a suitable password within the rule (a malicious user could disable that if they really wanted to) 

•	Index.php 

This will be the home page, displaying a welcome message. 

•	Signup.php 

Allowing username and password to be entered. 

Function used  checkUser 

A request Is made to the program checkuser.php (this report whether the username user is available) 

The returned result of the asynchonouse call (performed using JQuery) 

Function used SanitizerString 

To remove potentially malicious characters before looking up the username in the database, if not already taken (inserting the new username $user and password $pass)

Successfully signing up >>> Logging in  

Once logged in, user can visit 

Their profile (profile.php)
Their friends (friend.php)
Members details (members.php)
Messages and posts 
Logout option 

To make the code more user friendly. There needs to be error-handling routines, for example, user can catch any typographical or any other errors that might come and display error messages. Further, to keep security strong, if a user enters wrong password or wrong username, the screen will not show that they have entered the wrong password/name. Instead, it will show a message ‘Invalid login attempt’. 
