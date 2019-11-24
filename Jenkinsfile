pipeline {
    agent {
        label "master && linux"
    }

    environment {
        script {
            def props = readProperties file: '.env'
            SIMPLE_ENV = props.SIMPLE_ENV
        }
    }

    stages {
        stage('Execute Command 1') {
            steps {
                sh "env"
            }
        }
        stage('Execute Command 2') {
            steps {
                sh "env"
            }
        }
        stage('Execute Command 3') {
            steps {
                sh "env"
            }
        }
    }
}
