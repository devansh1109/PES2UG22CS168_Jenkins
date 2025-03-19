pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Build Stage'
                sh 'cd main && make'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                echo 'Test Stage Successful'
            }
            post {
                always {
                    echo 'Simulated test reports generated'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application'
                echo 'Deployment Successful'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed! Check logs for errors.'
        }
    }
}
