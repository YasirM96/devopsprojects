# devopsprojects
Jenkins Pipeline Scripts for Web Application


Pipeline Overview
The Jenkins pipeline consists of the following stages:

Fetch code: This stage fetches the latest source code of the vprofile application from the GitHub repository.

Build: In the build stage, the application is compiled and packaged using Maven, skipping the execution of tests.

Test: The test stage executes unit tests for the vprofile application using Maven.

Checkstyle Analysis: In this stage, a Checkstyle analysis is performed on the codebase using Maven.

Sonar Analysis: The Sonar Analysis stage analyzes the codebase using SonarQube, providing insights into code quality and metrics.

Quality Gate: This stage waits for the SonarQube Quality Gate to pass or fail before proceeding. You can configure the pipeline to abort if the Quality Gate fails.

UploadArtifact: The UploadArtifact stage uploads the vprofile application artifact (war file) to the Nexus repository.

