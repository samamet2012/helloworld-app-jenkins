pipeline {
    agent any

    tools {
        maven 'M2_HOME'  
    }

    stages {

        stage('Build') {
            steps {
                echo 'Build Step'
                sleep 10
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }

        stage('Test') {
            steps {
                echo 'Test step'
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Step'
                sleep 10
            }
        }

        stage('Docker') {
            steps {
                echo 'Image step'
            }
        }
    }
}
