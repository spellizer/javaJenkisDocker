pipeline {
    agent {
        docker {
            image 'maven:3.8-openjdk-8'
        }
    }
    stages{
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'maven test'
            }
        }
        stage('QA') {
            steps {
                echo 'QA'
            }
        }
    }
}