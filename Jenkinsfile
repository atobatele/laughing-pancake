node('docker') {
    checkout scm
    stage('Build') {
        docker.image('node:latest').inside {
            sh 'npm --version'
        }
    }
}
