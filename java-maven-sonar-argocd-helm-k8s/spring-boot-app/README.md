# Spring Boot based Java web application
 
This is a simple Sprint Boot based Java application that can be built using Maven. Sprint Boot dependencies are handled using the pom.xml 
at the root directory of the repository.

This is a MVC architecture based application where controller returns a page with title and message attributes to the view.

## Execute the application locally and access it using your browser

Checkout the repo and move to the directory

```
git clone https://github.com/iam-veeramalla/Jenkins-Zero-To-Hero/java-maven-sonar-argocd-helm-k8s/sprint-boot-app
cd java-maven-sonar-argocd-helm-k8s/sprint-boot-app
```
## Install maven

          sudo apt update

          sudo apt install maven -y

 # Check verification

          mvn -v
 
Execute the Maven targets to generate the artifacts

```
mvn clean package
```

The above maven target stroes the artifacts to the `target` directory. You can either execute the artifact on your local machine
(or) run it as a Docker container.

** Note: To avoid issues with local setup, Java versions and other dependencies, I would recommend the docker way. **


### Execute locally (Java 11 needed) and access the application on http://localhost:8080

```
java -jar target/spring-boot-web.jar
```

### The Docker way

Build the Docker Image

```
docker build -t ultimate-cicd-pipeline:v1 .
```

```
docker run -d -p 8010:8080 -t ultimate-cicd-pipeline:v1
```

Hurray !! Access the application on `http://<ec2 ip-address>:8010`


## Next Steps

### Configure a Sonar Server locally

```
System Requirements
Java 17+ (Oracle JDK, OpenJDK, or AdoptOpenJDK)
Hardware Recommendations:
   Minimum 2 GB RAM
   2 CPU cores
sudo apt update && sudo apt install unzip -y
adduser sonarqube
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.4.1.88267.zip
unzip *
chown -R sonarqube:sonarqube /opt/sonarqube
chmod -R 775 /opt/sonarqube
cd /opt/sonarqube/bin/linux-x86-64
./sonar.sh start
```

Hurray !! Now you can access the `SonarQube Server` on `http://<ip-address>:9000` 

username: admin
pwd: admin

# Authenticat sonarqube with jenkins

Goto Sonarqube --- myaccount -- security

![image](https://github.com/user-attachments/assets/a0057252-c599-4ad0-8e12-14e097403e93)

Goto Jenkins -- manage jenkins -- credentials -- Global credentials -- Addcredentials

![image](https://github.com/user-attachments/assets/88adfd43-98a2-40d5-95d6-191d804178b8)

# Install minikube and kubectl
for installation follow minikube&kubectl installation file(Installation repo)



# Install argocd using operators

goto this link:  https://operatorhub.io/operator/argocd-operator

clik on install and do all 

![image](https://github.com/user-attachments/assets/05255830-29c3-464c-974a-b17b0a20504d)



