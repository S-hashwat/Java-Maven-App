# Java Maven App - Jenkins CI Pipeline

This is a simple Java application managed using Maven and deployed via Jenkins. 
This project demonstrates how to set up a Jenkins pipeline that fetches code from GitHub and builds a Java application using Maven.

## 🚀 Tech Stack

- Java
- Maven
- Jenkins
- Git & GitHub

---


---

## ⚙️ Jenkins Setup Instructions

### 1. Install Jenkins (via Docker) using this command 
docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts

### 2. Unlock Jenkins
- Copy the admin password from your terminal:
use this command cat /var/jenkins_home/secrets/initialAdminPassword
- Paste it into the Jenkins setup screen in your browser.

### 3. Install Required Plugins
 - Git Plugin
 - Maven Integration Plugin

### 4. Add Tools
Go to: Manage Jenkins → Tools
- Add Git (auto-install)
- Add Maven (auto-install or point to your local Maven)

🔧 Job Configuration in Jenkins
1. Create a Freestyle Project
Name: java maven job

2. Configure Git Repository
GitHub Repo URL:
https://github.com/S-hashwat/Java-Maven-App

Branch to build:
*/main

3. Build Step
Select: Invoke top-level Maven targets

Goals:
clean package

4. (Optional) Post-Build Action
- Archive the artifacts:

✅ Output
If configured correctly, Jenkins will:
- Clone the GitHub repo
- Compile and package the Java code using Maven
- Generate a .jar file in the target directory
- Mark the build as SUCCESS

📌 Note
Ensure your GitHub repo’s branch name is set correctly (main or master) in the Jenkins configuration.




