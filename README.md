# SimpleServletApp README

## Description
This Java servlet application responds to GET and POST requests. It's built with Ant for easy compilation and packaging, and is designed to run on Apache Tomcat.

## Prerequisites
- JDK 8 or higher
- Apache Ant
- Apache Tomcat at `/usr/local/sdkman/candidates/tomcat/10.1.14`

## Project Structure
- `src/`: Source files for the servlet.
- `WebContent/`: Web files and WEB-INF directory.
- `WebContent/WEB-INF/web.xml`: Servlet configuration.
- `build.xml`: Ant build script located at the project root.
- `lib/`: Directory for library dependencies at the project root.

## Building and Deploying
1. **Include Servlet API**:
   - Download `servlet-api.jar`.
   - Place it in the `lib/` directory.

2. **Build with Ant**:
   - `build.xml` should be at the root of your project directory.
   - Run `ant` to compile and package the application into `dist/SimpleWebApp.war`.

3. **Deploy on Tomcat**:
   - Stop Tomcat: `./catalina.sh stop` from the Tomcat bin directory.
   - Copy `dist/SimpleWebApp.war` to the `webapps` directory of Tomcat.
   - Start Tomcat: `./catalina.sh start`.

4. **Access the Servlet**:
   - Visit `http://localhost:8080/SimpleWebApp/SimpleServlet`.

5. **Test POST Method**:
   - Use `curl` or Postman to send a POST request to the servlet's URL.

Follow these instructions for setting up, building, and deploying your servlet application.
