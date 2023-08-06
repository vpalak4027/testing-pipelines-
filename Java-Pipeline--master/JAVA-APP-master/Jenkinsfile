pipeline {
    agent any

    stages {
        stage('cloning the code from GitHub') {
            steps {
                git 'https://github.com/RAKHEE001/JAVA-APP.git'
            }
        }
        
        stage('Building the code') {
            steps {
                sh 'mvn clean install'
                
            }
        }
        
        stage('archiving the artifact') {
            steps {
                archiveArtifacts artifacts: 'target/maven-web-application.war', followSymlinks: false
            }
        }
    }
}
