pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages{
        stage('Build') {
            steps{
                sh 'mvn clean package'
            }
        }
        stage('test') {
            steps {
                sh " mvn test"
            }
            post {
                always {
                    junit '**/target/*.xml'
                }
            }
        }
        stage('deploying') {
            steps {
                echo "deploying"
            }
        }
    }
}
