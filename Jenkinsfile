pipeline {
    agent any  // Runs on any available agent

    stages {
        stage('Trigger Build Job') {
            steps {
                echo 'Triggering Build Job...'
                build job: 'Job1_Build'
            }
        }

        stage('Trigger Test Job') {
            steps {
                echo 'Triggering Test Job...'
                build job: 'Job2_Test'
            }
        }

        stage('Trigger Deploy Job') {
            steps {
                echo 'Triggering Deploy Job...'
                build job: 'Job3_Deploy'
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

