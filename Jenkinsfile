def getenv(String envname) {
    return sh(script: ". ./.env && printenv $envname || echo \$?", returnStdout: true).trim()
}

pipeline {
    agent {
        label "master && linux"
    }

    environment {
        SIMPLE_ENV = getenv("SIMPLE_ENV")
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
