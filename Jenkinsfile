pipeline {
    agent any

    environment {
        // اسم الـ credential اللي درتيه في Jenkins
        GIT_CREDENTIALS_ID = 'github-pat'
        REPO_URL = 'https://github.com/BOUSSELHAMYIYKI/my-projectSPRINT.git'
        BRANCH_NAME = 'main'
    }

    stages {
        stage('Checkout') {
            steps {
                // Clone repo باستخدام credential
                git(
                    url: env.REPO_URL,
                    branch: env.BRANCH_NAME,
                    credentialsId: env.GIT_CREDENTIALS_ID
                )
            }
        }

        stage('Build') {
            steps {
                echo "Build stage running..."
                // هنا تحط أي build command، مثلا Maven أو Gradle
                sh 'echo "Build command placeholder"'
            }
        }

        stage('Test') {
            steps {
                echo "Test stage running..."
                sh 'echo "Test command placeholder"'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy stage running..."
                sh 'echo "Deploy command placeholder"'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs for details.'
        }
    }
}
