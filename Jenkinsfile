pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('myflaskapp')
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    docker.image('myflaskapp').run('-p 5000:5000')
                }
            }
        }
    }
}
