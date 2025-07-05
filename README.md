# Java-based-Student-Registration-Web-Application
Deploy a Java-based Student Registration Web Application on AWS with proper  database integration and secure reverse proxy access using open-source tools.

1. Infrastructure Setup
EC2 Instances:
Instance 1: Reverse Proxy (Nginx)
Instance 2: Java Web Application (Tomcat)

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/901991c6-cc11-45fc-814a-1a961a602676" />



2. Application Deployment:

<img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/0c68d2b4-f208-4129-9cea-0e26a3f0e3df" />

Ensure it is running and accessible internally on port 8080

<img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/3e6f7a22-d432-4439-a878-b8f5b3d2dedc" />

Copy the application files onto the server:
C:\Users\tejas>scp -i Downloads\nverginiakeypair.pem Downloads\student.war ec2-user@107.21.154.91:.
student.war                                                                                                                               100%   87KB  48.3KB/s   00:01

3. Database Setup:
install Database
   <img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/83803125-a9f0-4684-aa0c-525b68cef874" />

   
connect with Ec2 instance:

<img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/c2f513fa-bc48-477f-b64a-8aaeda847b15" />

4. Database Connector Configuration:

The mysql-connector.jar file allows your Java application to communicate with the MySQL database using JDBC.

You uploaded it to your EC2 instance and moved it into Tomcat’s lib directory so it’s accessible to your web app.

Restarting Tomcat ensures the connector is loaded, enabling database operations like insert, update, and fetch.
C:\Users\tejas>scp -i Downloads\nverginiakeypair.pem "Downloads\mysql-connector(1).jar"  ec2-user@107.21.154.91:.
mysql-connector(1).jar                                                            100%  984KB 120.3KB/s   00:08


5. Reverse Proxy Configuration
   nginx installation on Instance 1: Reverse Proxy (Nginx)

<img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/43f5f1cd-2039-4580-a6d3-1c707d23eb80" />

Configured Nginx to forward traffic to the backend server on port 8080.

<img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/8f4faf98-2ca3-4fe1-9371-2152d142cd58" />

6 Access and URL Setup:
http://13.222.179.72/
<img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/688dee0c-af2c-48ef-8619-0d3b51c307e0" />





