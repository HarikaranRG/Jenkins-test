pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build steps here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add your test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy steps here
            }
        }
    }
    post {
        always {
            mail to: 'harichithran@gmail.com',
                 subject: "Email Notification: ${currentBuild.fullDisplayName}",
                 body: "Build details:\n\n${env.BUILD_URL}"
        }
    }
}
