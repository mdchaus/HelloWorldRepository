pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/mdchaus/HelloWorldRepository.git'
            }
        }

        stage('Hello') {
            steps {
                       echo 'Hello, Jenkins!'
            }
        }

        stage('Deploy') {
            steps {
                sh 'scp -i target/app.jar ubuntu@13.49.46.127:/home/ubuntu/'
                sh 'ssh -i ubuntu@13.49.46.127 "nohup java -jar /home/ubuntu/app.jar &"'
            }
        }
    }
}
