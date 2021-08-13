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
            docker ps
            docker version
            cd ..
            """)
            }
        }
    }
}
// pipeline {
//     agent any

//     stages {
//         stage('Hello') {
//             steps {
//                 echo 'Hello World'
//             }
//         }
//         stage('GoodBye') {
//             steps {
//                 echo 'Goodbye World'
//             }
//         }
//          stage('pwsh Hello') {
//             steps {
//                 powershell 'Write-Output "Hello PowerShell!"'
//             }
//         }
//     }
// }
