def getenv(String envname) {
    return """${sh(returnStdout: true, script: 'source .env && echo $${envname}')}""".trim()
}

pipeline {
    agent {
        label "master && linux"
    }

    environment {
        SIMPLE_ENV = getenv('SIMPLE_ENV')
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
