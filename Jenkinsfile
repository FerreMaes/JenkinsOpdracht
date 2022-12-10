pipeline {
  agent {
    docker {
      image 'node:10'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm run build'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Publish') {
      steps {   
          sh 'docker build -t ferremaes/Opdracht-Jenkins-image'
          sh 'docker push ferremaes/Opdracht-Jenkins-image'
      }
    }
  }
  triggers {
    githubWebHook()
    pollSCM('H/15 * * * *')
  }
}
