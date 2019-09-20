pipeline {
    agent {
        docker {
            image 'xabber'
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
                sh 'printf "2\n$(pwd)\n\n\n\nfoo\n" | ./xabberserver_installer.bin'
            }
        }
    }
}
