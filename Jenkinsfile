pipeline {
    agent any
    
    tools {
        maven "maven"
    }
    
    stages {
        stage("one") {
            steps {
                sh "rm -rf /root/.m2/repository"
            }
        }
        stage("two") {
            steps {
			  
                sh "mvn clean install"
            }
        }
        stage("three") {
            steps {
                sh "cp/root/.jenkins/workspace/project/target/LoginWebApp.war  /root/tomcat/webapps"
                sh "chmod -R 777 /root/tomcat"
            }
        }
    }
}


