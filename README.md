+ <b>Author: Moole Muralidhara Reddy</b></br>
+ <b>Email:</b> techworldwithmurali@gmail.com</br>
+ <b>Website:</b> techworldwithmurali.com , devopsbymurali.com</br>
+ <b>Description:</b> Below are the steps outlined for manually building and pushing artifacts(war) to Jfrog Artifactory</br>

## Manually - Build and Push to Jfrog Artifactory

### Prerequisites:
+ Git is installed
+ Maven is installed
+ Jfrog Artifactory is installed

### Step 1: Clone the repository
  
```xml
  github url: https://github.com/techworldwithmurali/nodejs-application.git
  branch name:
```


```xml
 <distributionManagement>
      <snapshotRepository>
        <id>jfrog-snapshots</id>
        <url>http://your-host:8081/repository/maven-snapshots/</url>
      </snapshotRepository>
      <repository>
        <id>jfrog-releases</id>
        <url>http://your-host:8081/repository/maven-releases/</url>
      </repository>
    </distributionManagement>
```
### Step 3: Update the jfrog credentials in settings.xml
```xml
<servers>
    <server>
      <id>jfrog-snapshots</id>
      <username>admin</username>
      <password>admin123</password>
    </server>
    <server>
      <id>jfrog-releases</id>
      <username>admin</username>
      <password>admin123</password>
    </server>
  </servers>
```
### Step 4: Run the below command to push the artifacts to Jfrog Artifactory.
```sh
mvn deploy
```
### Step 5: Verify whether artifact(war) is published or not in Jfrog Artifactory.
<p align="center">
  <img width="400" src="https://user-images.githubusercontent.com/115227391/210243233-12497d72-52e7-4e7f-bb9d-eef7d6fadf99.png" alt="cli output"/>
</p>


#### Congratulations. You have successfully Published the artifact(war) file in Jfrog repository.

### Authour
Moole Muralidhara Reddy
