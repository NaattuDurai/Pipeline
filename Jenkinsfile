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
               setx PATH "%PATH%;%JAVA_HOME%\bin"
setx PATH "%PATH%;%MAVEN_HOME%\bin"
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









