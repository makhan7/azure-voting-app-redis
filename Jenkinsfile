pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
              echo "${env.GIT_BRANCH}"
            }
        }
        stage('Docker Build'){
            steps{
       pwsh -command "docker images -a"
            }
        }
    }
}
