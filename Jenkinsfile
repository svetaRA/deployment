pipeline {

    agent any
    tools {
        maven 'maven_3_6_0' 
    }
    stages {
        stage('Compile stage') {
            steps {
                bat "mvn clean compile" 
        }
    }

         stage('testing stage') {
             steps {
                bat "mvn test"
        }
    }

          stage('install stage') {
              steps {
                bat "mvn install"
        }
		  }
              stage('deployment stage') {
              steps {
                
 "copy C:/Users/dell/.jenkins/workspace/AutoDeployment/target*.war D:/apache-tomcat-7.0.92/webapps"
        }
    }

  }

}
