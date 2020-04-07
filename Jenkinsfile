pipeline {
    agent { docker { image 'node:latest' } }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
                sh 'node --version'
                sh 'npm install'
                sh 'npm test'

            }
        }
        post {
          always {
            steps{
              junit 'output/*.xml'
            }
            script {
              echo 'stage always'
            }
        }
    }
}
