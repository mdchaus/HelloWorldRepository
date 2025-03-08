
pipeline {
    agent any

   
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'master', url: 'https://github.com/mdchaus/HelloWorldRepository.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  // Compiles, tests, and packages the application
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'  // Runs unit tests
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                // Add deployment steps here if needed
            }
        }
    }
}

