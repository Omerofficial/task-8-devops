# 🚀 Task 8 - DevOps Internship: Java Maven Build with Jenkins

This repository is part of my DevOps internship where I demonstrate how to set up and run a simple Java Maven project using Jenkins. The task introduces key CI/CD concepts by building a basic "Hello, World!" Java app via a Jenkins pipeline.

---

## 📁 Project Structure

hello-java-maven/ ├── pom.xml └── src/
 └── main/ └── java/ └── HelloWorld.java

 
- `HelloWorld.java`: Simple Java program that prints a message.
- `pom.xml`: Maven build configuration file.

## 🛠 Tools Used

- **Jenkins** (running via Docker)
- **Java JDK 11**
- **Apache Maven**
- **GitHub** (code hosted [here](https://github.com/Omerofficial/task-8-devops))

## 🚀 Steps Followed

1. Created a basic Java program (`HelloWorld.java`) that prints `Hello, Jenkins + Maven!`.
2. Configured Maven using a `pom.xml` file.
3. Ran Jenkins in a Docker container:
   ```bash
   docker run -p 8080:8080 jenkins/jenkins:lts

   
- `HelloWorld.java`: Simple Java program that prints a message.
- `pom.xml`: Maven build configuration file.

Configured tools inside Jenkins:

Added Maven in Global Tool Configuration

Set up JDK manually (linked to system path)

Created a Freestyle Project in Jenkins:

Pulled code from GitHub repo

Used mvn clean package as the build goal

Fixed JAVA_HOME issues by installing Java inside Jenkins container and exporting the path.

Triggered the build and verified successful output (BUILD SUCCESS).


![Screenshot (140)](https://github.com/user-attachments/assets/a5413fa8-2927-43f7-b2e6-3407aaebe854)


🧠 Interview Prep (Q&A)
What is Jenkins?
Jenkins is an open-source automation server used for building, testing, and deploying code automatically as part of CI/CD.

How do you create a Jenkins job?

Go to Jenkins dashboard → “New Item” → Choose “Freestyle project” → Configure steps.

What is Maven used for?
Maven is a build automation tool used primarily for Java projects. It handles compilation, dependency management, and packaging.

How does Jenkins use Maven?
Jenkins invokes Maven goals (like clean and package) to compile code and create build artifacts (like JAR files).

Difference between compile and package in Maven?

compile: Compiles Java source code.

package: Compiles code and packages it into a JAR/WAR file.

Where do you configure tools in Jenkins?
Manage Jenkins → Global Tool Configuration

How do you debug a failed Jenkins build?

Check the Console Output

Look for errors in the logs (e.g., missing JAVA_HOME, missing dependencies, syntax errors, etc.)
