def getenv() {
    return sh(script: "export $(grep -v '^#' .env | xargs)", returnStdout: true).trim()
}

pipeline {
    agent {
        label "master && linux"
    }

    environment {
        _ = getenv()
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
