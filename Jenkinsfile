pipeline {
    agent any
    triggers { pollSCM('H/5 * * * *') }
    stages {
        stage('Build') {
            steps {
                sh "ls"
                sh "chmod +x hello_from_sh"
                sh "./hello_from_sh"
                echo "Successfully automated!"
                sh "echo Text to artifact >> file.txt"
            }
        }
        stage('Test') {
            steps {
                sh "cat file.txt"
            }
        }
    }
}
