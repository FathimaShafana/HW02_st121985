# Using Spring Boot for the first time

I have created a repository to demonstrate on how to get started working with a Spring Boot Framework. Spring Boot Framework has gained popularity mainly due to its simplicity. With Spring Boot, it easy for you to create Spring based Applications that can stand-alone and with production-grade. It lets you just run your applications without much fuss.
This is a quick demo for building a classic “Hello World!” endpoint which any browser can connect to which I worked for one of my assignment.

Before you start, make sure you have a working IDE (Eclipse or Visual Studio Code or IntelliJ IDEA or Spring Tools etc.) and a JDK.

Here are the few easy steps to start up your first Spring Boot Project.
    1.	Create a “web project” using start.spring.io 
          •	In the “Dependencies” dialog search for and add the “Spring web”.
          •	Hit the “Generate” button.
          •	Download the zip and unpack it into a folder on your computer.
                Note: Under Spring Boot, always choose the latest release.
    2.	Open up the project in your IDE and locate the DemoApplication.java file in the src/main/java/com/example/demo folder.
          •	Modify the content as in DemoApplication.java file as in this repository.
    3.	Run your first Java Application.
            Right-click to build and run in your IDE.
            Else, use mvnw spring-boot:run in Windows Command Prompt.
    4.	Open any of your browser and input the address http://localhost:8080/hello and press enter. And you get your response there.

Issues I encountered as a first-time user:

#01.	Error : Description Resource Path Location Type Failure to transfer org.apache.maven.shared:maven-shared-components:pom:22 from https://repo.maven.apache.org/maven2 was cached in the local repository, resolution will not be reattempted until the update interval of central has elapsed or updates are forced. Original error: Could not transfer artifact org.apache.maven.shared:maven-shared-components:pom:22 from/to central (https://repo.maven.apache.org/maven2): repo.maven.apache.org pom.xml /demo line 1 Maven Configuration Problem

I resolved it by updating as follows
    •	In Eclipse, Right-click on your project
    •	Choose Maven->"Update Project ...", make sure "Update Dependencies" is checked in the resulting dialog box and click OK.


Once this was fixed, I had an issue when I entered http://localhost:8080/hello to my browser. "web server failed to start. port 8080 was already in use".

I first tracked which process was using the port 8080 by the following line in command prompt.
  o	netstat -ano | findstr *<port used>*

Later killed that process using,
  o	taskkill /F /PID *<PID>*

and got my browser displaying “Hello World”.

Give a try to get your first Spring Boot Application…!!!


Reference:
 Spring.io. 2021. Spring Quickstart Guide. [online] Available at: <https://spring.io/quickstart> [Accessed 21 January 2021].
