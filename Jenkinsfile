pipeline {
    agent any

    tools {
        // This tells Jenkins to look for your global Maven installation
        maven 'maven-3' 
    }

    stages {
        stage('Checkout Source Code') {
            steps {
                // We explicitly define your new repository URL here
                git branch: 'master', url: 'https://github.com/Ayush-Modanwal/Library-Application-Testing.git'
            }
        }

        stage('Compile & Build') {
            steps {
                // Actually runs Maven instead of just printing text
                sh 'mvn clean compile'
            }
        }

        stage('Execute Unit Tests') {
            steps {
                // Actually runs your Java unit tests
                sh 'mvn test'
            }
        }
    }
}
