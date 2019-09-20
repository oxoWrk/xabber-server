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
                sh 'echo Test'
                sh 'pwd'
            }
        }
    }
}
