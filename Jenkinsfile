
pipeline {
    agent {
        label '!windows'
    }

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
        stage('Build') {
            steps {
                echo "Database engine is ${DB_ENGINE}"
                echo "DISABLE_AUTH is ${DISABLE_AUTH}"
                sh 'printenv'
            }
        }
    }
    post {
    always {
        
             echo "Failed Pipeline: ${currentBuild.fullDisplayName}"
             echo "Something is wrong with ${env.BUILD_URL}"
    }
}
}
