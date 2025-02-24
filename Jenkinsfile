pipeline {
    agent any  // Use any available Jenkins agent

    environment {
        APP_NAME = "SampleApp"
        BUILD_DIR = "build"
    }

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning repository from GitHub...'
                // Uncomment below for real project
                // git branch: 'main', url: 'https://github.com/your-repo/sample-project.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Simulated build step, replace with actual command
                // sh 'mvn clean install' (For Java)
                // sh 'npm install && npm run build' (For Node.js)
            }
        }

        stage('Unit Tests') {
            steps {
                echo 'Running unit tests...'
                // Simulated test step, replace with actual test command
                // sh 'mvn test' (For Java)
                // sh 'npm test' (For JavaScript)
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging application...'
                //sh "mkdir -p ${BUILD_DIR} && echo 'Build Artifacts' > ${BUILD_DIR}/artifact.zip"
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                // Simulate deployment (Replace with actual deployment steps)
                // sh 'scp target/app.jar user@staging-server:/deploy-path/'
            }
        }

        stage('Deploy to Production') {
            when {
                branch 'main' // Deploy only if it's the main branch
            }
            steps {
                echo 'Deploying to production...'
                // Simulate production deployment
                // sh 'scp target/app.jar user@prod-server:/deploy-path/'
            }
        }
    }

    post {
        success {
            echo '✅ CI/CD Pipeline executed successfully!'
        }
        failure {
            echo '❌ CI/CD Pipeline failed! Please check the logs.'
        }
    }
}

