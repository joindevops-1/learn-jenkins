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
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
               sh """
                    echo  "this is deploy stage"
                """
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'I will run while pipeline is failed'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
    }
}