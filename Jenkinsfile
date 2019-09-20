pipeline {
    agent {
        docker {
            image 'xabber'
            args '-u root'
            }
    }
    stages {
        stage('Build') {
            steps {
                sh './create_xabber_release'
            }
        }
        stage('Test') {
            steps {
                sh 'printf "2\n\n\n\n\n\n" | ./xabberserver_installer.bin'
            }
        }
    }
}
