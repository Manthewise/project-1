# project-1

project overview 

This project demonstrates how to deploy and manage a Node.js application in a production-like environment using PM2.
The goal is to simulate how backend applications are managed on Linux servers.

Technologies used 

 Node.js
 npm
 PM2
 Linux (Ubuntu / WSL)

project structure

'''text
pm2-project/
├── app.js
├── package.json
└── README.md
'''

Application Code
'''javascript
const http = require("http");

const server = http.createServer((req,res)=>{
 res.end("DevOps Project 2 running with PM2");
});

server.listen(3000);
'''
This simple server listens on port 3000.

installation 

sudo apt update
sudo apt install nodejs npm
npm install -g pm2

Running the Application

Start the app normally:
node app.js
Run using PM2:
pm2 start app.js
Check running processes:
pm2 list

PM2 Features Demonstrated
•	Process management
•	Automatic restart on crash
•	Background execution
•	Monitoring and logs

Commands used:
pm2 logs
pm2 monit
pm2 restart app

Auto Startup
Configure PM2 to restart apps after server reboot.
pm2 startup
pm2 save

What I Learned
Through this project I learned how production applications are managed on Linux servers.
I also practiced process management, monitoring, and service persistence using PM2.




