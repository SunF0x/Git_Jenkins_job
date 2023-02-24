pipeline {
    agent any
    triggers { pollSCM('H/5 * * * *') }
    stages {
        stage('Build') {
            steps {
                sh "ls"
                sh "chmod +x hello_from_sh"
                sh "./hello_from_sh"
            }

        }
    }
}
