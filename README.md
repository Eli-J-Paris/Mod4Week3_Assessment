# Week 3 Assessment

## Setup
* Fork and Clone this repository
* Run `update-database` - let the instructors know if you run into any issues!

## Exercise (10 Points)
### Securing the Application (4 points)
* Use Secrets Managemnt to remove the database connection string from the application.
* So that we can see the full implmentation, include a screenshot below to show your `secrets.json` file

<img width="928" alt="image" src="https://github.com/Eli-J-Paris/Mod4Week3_Assessment/assets/130601227/831ca0e2-bb34-4076-bedb-5a4cc4368cc3">


### Maintaining Current-User (6 points)

This application includes some starter code so that we could maintain a current user.  Review the Login and Logout code in the Home Controller, along with the Login and Logout buttons in the Home/Index.cshtml file.  Building on this pre-existing structure:
* Create a cookie that holds a key for "currentUser" when a user logs in.
* Delete that cookie when a user logs out.
* Add the value of "current user" to all views

## Questions (10 Points)

For the following questions, answer as if you are in an interview!
1. Describe one strategy you have used to maintain state in a web application. (2 points)
Considering HTTP is stateless and each request is isloated from others. This is limiting as often times as a developer you will need to use information or data from one request to the next. One way that I have used to keep track of this data is cookies. The main benefit of using cookies to store reaccuring pieces of data is that they are stored in the browser. So if you want a user to stay signed into your website you could create a cookie that remembers them so that they are already signed in to your website after they leave and come back
2. How would you protect sensitive data that we need to store in our database - for example, passwords? (2 points)
One way of the best way to store sensitive data is running that data through a hash function. This is a great algorithm for coding any length of data into a fixed size. This allows passwords to be stored in a randow string in the DB so hackers ever got a hold of them they would be hard pressed to reverse engineer them to what the orginal password was
3. Describe 3 additional common security risks in web development. (make sure you discuss what you know about the risk, and if you know how to minimize the risk) (6 points)
API rate limiting is one risk. the risk here is some one with malcious intent could make over load an API with requests shutting it down or prevenint other legitiate users from using the API, one way to counter this is by setting a limit to how many request can be made in a certain time frame.

SQL Injection is another risk. This is done by inserting SQL queries nto input fields that are typically used in database queries. if successful this could lead to unauthorized access. one way of preventing this is by santizing the input before it directly touches the database. IN general you dont want the input to go directly to your database.

Overpost Prevention is another sercurity concern. THis happens when someone try to change properties or fields by sending in more data than expected
