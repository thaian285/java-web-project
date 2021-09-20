pipeline {
    agent any
    stages {
        stage("Build") {
    	   steps{
                  sh 'mvn clean package'
    	   }
        }
        stage("Deploy") {
    	   steps {
                  deploy adapters: [tomcat7(credentialsId: 'b8665114-e3b8-44c8-8e00-19fd2be7d341', path: '', 
                  url: 'http://34.203.240.133:8080/')], 
                  contextPath: 'javawebapp', war: '**/java-web-project.war'
    	   }
        }
    }
}
