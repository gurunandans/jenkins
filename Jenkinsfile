pipeline {
    agent any  // Use any available Jenkins agent

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Print Node Version') {
            steps {
                sh 'node -v'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App or Test') {
            steps {
                sh 'npm start || npm test || echo "No start or test script found."'
            }
        }
    }

    post {
        always {
            echo 'Pipeline run completed.'
        }
    }
}
