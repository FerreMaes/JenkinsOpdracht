pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t my-app .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                sh 'docker login -u ferremaes -p PDG2002m'
                sh 'docker push my-app'
            }
        }
    }
}
