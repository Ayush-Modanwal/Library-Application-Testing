pipeline {
    agent any

    tools {
        maven 'Maven 3.x' // Make sure this matches your Jenkins Global Tool Configuration name
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Ayush-Modanwal/Library-Application-Testing.git'
            }
        }

        stage('Compile & Build') {
            steps {
                // This tells Jenkins to actually compile the Java code
                sh 'mvn clean compile'
            }
        }

        stage('Execute Unit Tests') {
            steps {
                // This tells Jenkins to run your test classes
                sh 'mvn test'
            }
        }
    }
}
