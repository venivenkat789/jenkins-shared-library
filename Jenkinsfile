@Library('my-shared-lib') _

pipeline {
    agent any

    tools {
        maven 'maven3.9.12'
        jdk 'java17'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/venivenkat789/simple-java-maven-app.git'
            }
        }

        stage('Build') {
            steps {
                mavenBuild()   // calling shared library function
            }
        }

        stage('Post-Build') {
            steps {
                echo "Build completed successfully."
            }
        }
    }
}
