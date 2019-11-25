def getenv(String envname) {
    def result = readProperties file: '.env'
    return result[envname]
}

pipeline {
    agent {
        label "master && linux"
    }

    environment {
        SIMPLE_ENV = getenv("SIMPLE_ENV")
        MASK_VAR = getenv("MASK_VAR")
        VM_COUNT = getenv("VM_COUNT")
    }

    stages {
        stage('Execute Command 1') {
            when {
                expression {
                    VM_COUNT > 0
                }
            }
            steps {
                sh "env"
                echo "Create Instance"
            }
        }
        stage('Execute Command 2') {
            when {
                expression {
                    VM_COUNT == 0
                }
            }
            steps {
                sh "env"
                echo "Destroy Instance"
            }
        }
        stage('Execute Command 3') {
            steps {
                sh "env"
            }
        }
    }
}
