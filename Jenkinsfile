pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mkdir -p /var/www/html'
            }
        }
    }
}
