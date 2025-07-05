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

   <img width="960" height="540" alt="Image" src="https://github.com/user-attachments/assets/83803125-a9f0-4684-aa0c-525b68cef874" />


