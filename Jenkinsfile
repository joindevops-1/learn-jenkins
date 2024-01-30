pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    } 
    stages {
        stage('Build') { 
            steps {
                sh """
                    echo "this is build stage"
                """
            }
        }
        stage('Test') { 
            steps {
                sh """
                    echo "this is test stage"
                """ 
            }
        }
        stage('Deploy') { 
            steps {
               sh """
                    echo "this is build stage"
                """
            }
        }
    }
}