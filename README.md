# Maven-Tutorials


<h3>1. Build single JAR File for SWING like applications</h3>
you need to add below code to the POM and should specify main class
```
<build>
        <plugins>
            <plugin>
                <artifactId>maven-assembly-plugin</artifactId>
                <configuration>
                    <archive>
                        <manifest>
                            <mainClass>com.spacex.floggame.FlogClient</mainClass>
                        </manifest>
                    </archive>
                    <descriptorRefs>
                        <descriptorRef>jar-with-dependencies</descriptorRef>
                    </descriptorRefs>
                </configuration>
            </plugin>
        </plugins>
</build>
```
    Then go to project location which display pom.xml and execute below command
    mvn clean compile assembly:single
