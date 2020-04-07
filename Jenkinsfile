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
        stage('post') {
            steps {
                junit 'output/*.xml'


            }
        }



    }
}
