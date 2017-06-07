

# canvas-app


### About:   A Collaborative Message board


### Installing the PreRequisites:
- Be sure NodeJs vsn 6.0 or greater is installed. The email module (Nodemailer) won't work otherwise
- Also Install Mongo
- In order to get started using Mongo with your application (after it has been downloaded) follow the following steps:
    1) mkdir -p /data/db   , to create the directory where mongo will be writing data
    ##### In order to run mongo without sudo, the permissions of the data folder created in step i. must be changed if you         would like to do this move on to step ii. (otherwise you can just launch mongo after creating the data directory with         "sudo mongod" and move on to the "How to get started" section)
    2) "cd /"   , navigate to the root directory of your machine (or the directory where you created the data directory if 
    other than the root directory)
    3) "open ."  , running this command opens spotlight after navigating to the folder where the data directory is (done in       step 2)
    4) right click on the "data" folder create in step 1 and select "get info" option (a pop up window should appear at this     point)
    5) At the bottom of the window that should have appeared (in step 4) change privileges for all users to "READ & WRITE"       then click the gear at bottom also at the bottom of that same window and select "Apply to enclosed items"
    6) Now mongo can be run using "mongod" instead of "sudo mongod"
    
### How to get started:
  1) clone the project from github (git clone https://github.com/ehruska/canvas-app.git)
  2) cd canvas-app (change into newly cloned directory)
  3) In same terminal (1st terminal tab) "npm install" (to install the needed packages for the project)
  4) (In same terminal) run "node server.js"
  5) 2nd terminal tab) start mongo (with "mongod" if you followed the instructions above otherwise "sudo mongod")
  6) 3rd terminal tab) change into the "client" directory of the application "cd client"
  7) Once done (still in 3rd terminal tab) run "python -m SimpleHTTPServer 8888"
  8) Navigate to http://localhost:8888 (in a browser)
  
 (Note: line breaks in the code snippet below means the code should be run in a new terminal tab. Also same as above. The       code snippet is the same as the "How to get started" section)
```
git clone https://github.com/ehruska/canvas-app.git
cd canvas-app
npm install
node server.js

sudo mongod (in new terminal tab)

cd client (directory, in new terminal tab)
python -m SimpleHTTPServer 8888
Navigate to http://localhost:8888 (in a browser)
```

### How to run the tests
To run the tests make sure the tabs running the node server ("node server.js") and the tab running mongo ("mongod")
remain running. After having created a user or two in the client application and confirming the email verification of said user. Open the test.html file in the tests folder in a browser and the tests should be run. Note Test d) which tests the route /adjoinimg will create a new img every time the tests are run you can see the imgs being created if you have open the public/img/uploads directory as you reload the page
