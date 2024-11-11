
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Mohamed-Elhadad123/jenkens'  // Replace with your repository URL
            }
        }
       
               stage('Run file') {
            steps {
                script {
                    // Run the Docker container
                    chmod +x 'project'
                    sh './project'
                }
            }
        }
    }
    post {
       
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
