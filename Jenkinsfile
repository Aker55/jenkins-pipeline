pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven-3.9.4"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'master', changelog: false, credentialsId: 'GitHub credentials', poll: false, url: 'https://github.com/Aker55/maven.git'
            }
        }
        stage('maven'){
            steps {
                sh 'mvn clean install'
            }
        }   
    }
}

