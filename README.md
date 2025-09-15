# SIT223/753 – Task 8.1C – Jenkins Pipeline Design

This repository contains the Jenkinsfile for **Part 1 Task 1** of the Continuous Integration and DevSecOps task.  
It demonstrates a 7-stage pipeline design integrated with GitHub.

---

## Stage Descriptions

1. **Build**  
   Compile and package the application using a build automation tool such as **Maven** or **Gradle**.

2. **Unit and Integration Tests**  
   Run unit tests with tools such as **Jest** or **Mocha**, and integration tests with **Supertest** to ensure that components work correctly together.

3. **Code Analysis**  
   Perform static code analysis with tools like **ESLint**, **Checkstyle**, or **PMD** to enforce coding standards and detect issues early.

4. **Security Scan**  
   Identify vulnerabilities in dependencies using tools such as **OWASP Dependency-Check** or **Snyk**.

5. **Deploy to Staging**  
   Deploy the build to a staging environment (e.g., an **AWS EC2 instance**) for testing in a production-like setup.

6. **Integration Tests on Staging**  
   Run additional integration or API tests (e.g., **Postman/Newman**) against the staging environment to validate functionality.

7. **Deploy to Production**  
   Deploy the verified build to the production environment (e.g., **AWS EC2 instance**) for end users.

---

## How It Works
- Jenkins polls this GitHub repository every 2 minutes (`H/2 * * * *`).  
- When a commit is pushed, Jenkins automatically runs the pipeline defined in the `Jenkinsfile`.  
- Each stage prints a message to confirm successful execution.
- ✅ Test commit for Jenkins integration
-Last update: test for Jenkins auto-trigger
🔄 Test commit at 10:33 AM to trigger Jenkins

