@Library('my-shared-lib') _

pipeline {
    agent any
    tools {
        maven 'maven3.9.16'  // Use the Maven tool installed earlier
        jdk 'java21'        // Use JDK 17
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout the project from the 'project-1' branch in your GitHub repository
                git branch: 'main', url: 'https://github.com/srikanth78933/jenkins-shared-library.git'
            }
        }
        stage('Build') {
            steps {
                mavenBuild()  //calling shared library function
            }
        }
        stage('Post-Build') {
            steps {
                echo "Build completed successfully."
            }
        }
    }
}
