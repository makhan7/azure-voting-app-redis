pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                pwsh -command "docker images -a"
            }
        }
    }
}