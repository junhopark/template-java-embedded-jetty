# Embedded Jetty template application 

This is a template for a web application that uses embedded Jetty. This code was initially cloned from http://java.heroku.com/ (https://cloner.heroku.com/apps/template-java-embedded-jetty).

Upon cloning, the following updates were made:

* Include Twitter Bootstrap v3.0.0
* Updated to use Java 1.7
* Updated to use Jetty 9
* Updated to use Servlet 3.1.0, which allows for @WebServlet annotation usage (see: CurrentDateTimeServlet.java)
* Include SASS (See: src/main/webapp/styles/)
* Include PostgreSQL JDBC Driver

## Running the application locally

First build with:

    $mvn clean install

Then run it with:

    $java -cp target/classes:target/dependency/* com.jpark.Main

## Notes on using IntelliJ IDEA

I'm currently using IntelliJ IDEA 11 (Ultimate Edition).  To make this work with IntelliJ, follow these steps:

* After cloning, go to: File > New Project > Import project from external model > Next > Select 'Maven' > Next > Set 'Root directory' to the root of the project > Keep selecting Next with default options and close out of the modal.
* Go to: File > Project Structure > Project > Set 'Project language level' to 7.0.
* While you're still in Project Structure, select Artifacts > set the 'Output directory' to: [PROJECT ROOT]/target/embedded-jetty-template-1.0-SNAPSHOT > Check 'Build on make' > Click OK.
* Open Main.java > Right-click > Select Run 'Main.main()' or Debug 'Main.main()'.
* Open your browser and go to: http://localhost:8080

## See it live

http://embedded-jetty-template.herokuapp.com