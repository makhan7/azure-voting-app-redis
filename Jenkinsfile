pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                powershell "docker images -a"
                 powershell(script: """
            cd azure-vote/
            docker images -a
            docker build -t jenkins-pipeline .
            docker images -a
            cd ..
            """)
            }
        }
    }
}