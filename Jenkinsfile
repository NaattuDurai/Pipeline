pipeline {
    agent any

    tools {
        // Define Maven tool
        maven "Apache Maven 3.8.8"
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build the Maven project
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests (adjust the test command as needed)
                bat 'mvn test'
            }
        }

        stage('Archive Artifacts') {
            steps {
                // Archive the built JAR file (adjust the file name as needed)
                archiveArtifacts 'target/*.jar'
            }
        }
    }
}









