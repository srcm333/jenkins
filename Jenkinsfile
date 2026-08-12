pipeline {
    agent { 
        node { 
            label 'ROBOSHOP' 
        } 
    }
    environment {
        COURSE = "Jenkins"
    } 
    //Build
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo "Course is: ${COURSE}"
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }

    post {
        always {
            echo 'I will always say Hello again!'
        }
        success {
            echo 'I will Run when it success'
        }
        failure {
            echo 'I will Run when it is failed'
        }
    }
}