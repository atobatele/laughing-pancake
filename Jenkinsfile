pipeline {

    stages {
        stage('build') {
          agent { docker 'node:latest' }
            steps {
                  sh 'npm --version'
                  sh 'node --version'
                  sh 'npm install'
            }

        }
        stage('test') {
            agent { docker 'selenium/standalone-chrome:3.141.59' }
            steps {
                  sh 'npm install'

            }
        }
        stage('post') {
            agent { docker 'selenium/standalone-chrome:3.141.59' }
            steps {
                junit 'output/*.xml'
            }
        }



    }
}
