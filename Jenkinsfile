pipeline {
    agent any  // Runs on any available agent

    stages {
        stage('Trigger Build Job') {
            steps {
                echo 'Triggering Build Job...'
                build job: 'BUILD'
            }
        }

        stage('Trigger Test Job') {
            steps {
                echo 'Triggering Test Job...'
                build job: 'TEST'
            }
        }

        stage('Trigger Deploy Job') {
            steps {
                echo 'Triggering Deploy Job...'
                build job: 'DEPLOY'
            }
        }
    }

    post {
        success {
            echo '✅ All jobs executed successfully!'
        }
        failure {
            echo '❌ Pipeline failed! Check logs for errors.'
        }
    }
}

