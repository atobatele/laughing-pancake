pipeline {
    agent { docker { image 'node:latest' } }
    stages {
        stage('build') {
          script {
            docker.image("selenium/standalone-chrome:3.141.59"){
                sh 'npm --version'
                sh 'node --version'
                sh 'npm install'
                sh 'npm test'

            }
          }

        }
        stage('post') {
            steps {
                junit 'output/*.xml'


            }
        }



    }
}
