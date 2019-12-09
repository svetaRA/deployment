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
              stage('deployment stage') {
              steps {
                bat "deploy adapters: [tomcat7(credentialsId: 'admin', path: '', url: 'http://localhost:9090')], contextPath: null, war: 'target/JenkinsWar.war'"
        }
    }

  }

}
