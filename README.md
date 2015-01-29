# Checkstyle

Add the following plugin to your maven pom to reference this checkstyle.
This checkstyle is google's standard with line length adjusted to 140.
This plugin version supports Java 8 per the puppycrawl 6.2 dependency.
The eclipse-java-google-style.xml is the analogous formatter for eclipse.
To use it, load this xml style to eclipse and click "Format on Save".

    <plugin> 
       <groupId>org.apache.maven.plugins</groupId>
       <artifactId>maven-checkstyle-plugin</artifactId>
       <version>2.13</version>
       <executions> 
           <execution> 
               <id>checkstyle</id> 
               <phase>validate</phase> 
               <goals> 
                   <goal>check</goal> 
               </goals> 
           </execution> 
       </executions> 
       <configuration> 
         <consoleOutput>true</consoleOutput>
         <configLocation>https://rawgit.com/java-checkstyle/checkstyle/master/GoogleJavaCheckstyle-140.xml</configLocation> 
         <includeTestSourceDirectory>true</includeTestSourceDirectory> 
         <failsOnError>true</failsOnError> 
       </configuration> 
       <dependencies> 
           <dependency> 
               <groupId>com.puppycrawl.tools</groupId> 
               <artifactId>checkstyle</artifactId> 
               <version>6.2</version> 
           </dependency> 
       </dependencies> 
    </plugin> 
