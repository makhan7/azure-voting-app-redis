pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
              echo "${env.GIT_BRANCH}"
            }
        }
         steps {
                sh 'node --version'
            }
         stage('Docker Build'){
            steps{
        pwsh(script: 'docker images -a')
    }
    }
    }
}
