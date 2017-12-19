# JABR-Project-3-Services
See documentation.txt file under each service for end points and input/output values

JAB’R Project 3 Instructions 
Revature Repo
Angular GitHub Repo: 
Microservices GitHub Repo: https://github.com/revaturelabs/scrumboard-microservices-example.git
Config yml files Repo: 

Original Repo:
Angular GitHub Repo: https://github.com/rbunning/JABR-Project-3-Angular
Microservices GitHub Repo: https://github.com/rbunning/JABR-Project-3-Services
Config yml files GitHub Repo: https://github.com/rbunning/JABR-Project-3-config-yml-files
	*checkout branch localTestBranch for config yml files*

To run the project locally:
Pull the files from the Angular and Microservices GitHub Repos
Create new schemas in Oracle called (as shown in ddl.sql script in JABR-Project-3-Services GitHub Repository):
p3board
p3boardcomment
p3chart
p3story
p3task
p3user
Run ddl script under each schema as instructed in ddl.sql file
If you get errors about not having permission to allocate space in users tablespace:
Goto Other Users tab
For each p3* user, right click and select Edit User
Goto Quotas tab and check unlimited for Users tablespace
Run dml scripts under the appropriate schema (Except Chart and Task)
Install Erlang (https://www.erlang-solutions.com/resources/download.html)
Install RabbitMQ (https://www.rabbitmq.com/install-windows.html)
Using Spring Tool Suite, check the application.yml in the config service file to verify that the localTestBranch is set as the default branch.
Add the ojdbc7.jar dependency in the resources/static folder to the  story, task, comment, chart services.
Do a Maven Update to get all the dependencies
Start Spring Boot applications in the following order Config, Eureka, user, Zuul, board, story, task, comment, chart.
(Optional) Restart Zuul service to speed up the finding of services by Zuul.
Using Visual Studio Code, open JABR-Project-3-Angular folder 
Using integrated powershell terminal in Visual Studio Code, or any command line, run these commands:
npm install -g angular-cli (optional, if angular-cli is not installed globally) 
If failed try
npm install -g @angular/cli 
npm install 
npm update
npm start (ng serve will not work because we are using json proxy)
Using any Web Browser (Google Chrome recommended) 
Type localhost:4200 in the address bar to view the application 
To login to the application:
For least privilege:
Username: user
Password: user
or for most privilege:
Username: scrum
Password: scrum





