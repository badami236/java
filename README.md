docker:
login docker
create folder on desktop
drag and drop the fld to vs code
create file on vs code:
  dockerfile
  index.html
dockerfile,inside
  From httpd:latest
  COPY index.html/user/local/apache2/htdocs/
index.html
  <!DOCTYPE>
  <P>
    HELLOWORLD>
  </P>
open terminal
  type: docker build -t mywebsite .
  type: docker run -d --name mywebsite-container -o 9092:80 mywebsite
  open



maven:
open eclipse
create new maven project
select catalog
       internal
       maven-quickstart1.1
put name-> group id and artifact id
got to src/test/java
   create class->Readjson
right clk on project and create new folder
   right clk on folder and create new file
    student.json  :
{
  "name": "Rahul",
  "age": 21,
  "branch": "ISE",
  "college": "VVCE"
}

pom.xml->         

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>maju</groupId>
  <artifactId>abhi</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>jar</packaging>

  <name>abhi</name>
  <url>http://maven.apache.org</url>

  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
  </properties>

  <dependencies>
    <dependency>
             <groupId>com.googlecode.json-simple</groupId>
            <artifactId>json-simple</artifactId>
            <version>1.1.1</version>
    </dependency>
  </dependencies>
</project>


readjson:   

import java.io.FileReader;
import org.json.simple.JSONObject;
import org.json.simple.parser.JSONParser;

public class Readjson {
    public static void main(String[] args) {
        try {
            JSONParser parser = new JSONParser();

            FileReader reader =
                new FileReader("JSON/student.json");

            JSONObject student =
                (JSONObject) parser.parse(reader);

            System.out.println("Name: " + student.get("name"));
            System.out.println("Age: " + student.get("age"));
            System.out.println("Branch: " + student.get("branch"));
            System.out.println("College: " + student.get("college"));

            reader.close();

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}





exp4:

1.Login to Jenkins
2.login to github
3.create a new repository in github 
4.In new repository create a new file (test.java)
5. write a simple java code inside test.java and save the file
6. In Jenkins create a free style project (labprogram7)
7.In Jenkins go to manage Jenkins > select plugins > click on available plugins > search for git > then install
8. click on the project > configure > go to source code management >select Git > paste the repository url  with .git > select windows execute batch command >
Javac test.java
Java test                    >   save
9. select github webhooks 
10. run the project in Jenkins



exp 5:
1.Login to Jenkins
2.Create a new free style project
3.Click on manage Jenkins > select plugins > in available plugins search for slack and install 
4.login to slack 
5. Switch to workspace > create a new channel > click on Apps > browse apps > search for Jenkins CI > open Jenkins CI > click on configurations > Add to slack > select the channel which you have created > 
6.In Step3 : copy the secret credential  
7.come back to Jenkins > click on manage Jenkins > System > slack > Add workspace name > Add Jenkins > kind select secret text > paste the Secret ID > select default channel >  
8. click on “Test Connection”
9. post build actions > select when project built success, failure, abort > apply , OK
10. Build the project 



exp1:
class hello{
    void main(String [] args){
        System.out.print("hello");
    }
}


git init
git add .
git commit -m "initial commit"
git branch b1
git switch b1
git add .
git commit -m "b1"
git switch master
git branch b2
git switch b2
git add .
git commit -m "b2"
git switch b1
git switch master
git merge b1
git merge b2
