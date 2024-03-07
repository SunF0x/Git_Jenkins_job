pipeline {
    agent any //agent { node { label 'sdCloud_docker_deploy' } }
    triggers { pollSCM('H/5 * * * *') }
    stages {
        stage('Preparation') {
            steps {
                step([$class: 'WsCleanup'])
                checkout scm
            }
        }
        stage('Build application') {
            steps {
                sh "ls"
                sh "chmod +x hello_from_sh"
                sh "./hello_from_sh"
                echo "Successfully automated!"
                sh "echo Text to artifact2 >> file.txt"
            }
        }
        stage('Deploy artifacts') {
            steps {
                sh "cat file.txt"
            }
        }
    }
}
