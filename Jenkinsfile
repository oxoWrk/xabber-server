pipeline {
    agent none
    
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'xabber'
                }
            }
            steps {
                sh './create_xabber_release'
            }
        }
        stage('Test') {
            agent any
            steps {
                sh 'printf "2\n\n\n\n\n\n" | ./xabberserver_installer.bin'
            }
        }
    }
}
