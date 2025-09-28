pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "This is build stage"
            }
        }
        stage('Test') {
            steps {
                echo "This is test stage"
            }
        }
         stage('Docker image build') {
            steps {
                echo "This is docker image build stage"
            }
        }
        stage('Deploy') {
            steps {
                echo "This is deploy stage"
            }
        }
    }
}
