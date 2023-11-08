# SimpleServletApp README

## Description
This is a basic Java servlet application demonstrating handling GET and POST requests. The build and deployment process utilizes Apache Ant and the app is deployable on Apache Tomcat.

## Prerequisites
- JDK 8 or above installed
- Apache Ant installed
- Apache Tomcat 10.1.14 installed at `/usr/local/sdkman/candidates/tomcat/10.1.14`

## File Structure
- `src/`: Contains the servlet Java source files.
- `WebContent/`: Contains web content including WEB-INF.
- `lib/`: Contains all the necessary libraries.
- `build.xml`: Ant build script for the project.
- `web.xml`: Deployment descriptor file.

## Setup Instructions
1. **Include Servlet API**: 
   - Download the `servlet-api.jar` from the appropriate source.
   - Place it into the `lib/` directory of your project.

2. **Build the Application**:
   - Run `ant compile` to compile the servlet classes.
   - Execute `ant package` to create the WAR file in the `dist/` directory.

3. **Deploying on Tomcat**:
   - Stop Tomcat: `/usr/local/sdkman/candidates/tomcat/10.1.14/bin/catalina.sh stop`
   - Copy the WAR file to the `webapps` directory of Tomcat:
     ```
     cp dist/SimpleWebApp.war /usr/local/sdkman/candidates/tomcat/10.1.14/webapps/
     ```
   - Start Tomcat: `/usr/local/sdkman/candidates/tomcat/10.1.14/bin/catalina.sh start`

4. **Accessing the Servlet**:
   - Open a browser and go to `http://localhost:8080/SimpleWebApp/SimpleServlet`.

5. **Testing POST Method**:
   - Use a tool like `curl` or Postman to send a POST request to your servlet at `http://localhost:8080/SimpleWebApp/SimpleServlet`.

Make sure to follow each instruction carefully to ensure the servlet is compiled, packaged, and deployed correctly.
