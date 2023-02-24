pipeline {
    agent any
    triggers { pollSCM('* * * * *') }
    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                sh "ls"
                // git branch: 'main', url: 'https://github.com/SunF0x/Git_Jenkins_job.git'
                sh "ls"
                sh "chmod +x hello_from_sh"
                sh "./hello_from_sh"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}
