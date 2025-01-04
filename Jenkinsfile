@Library('shared-library') _

pipeline {
    agent any

    stages {
        stage('Call Shared Library Pipeline') {
            steps {
                script {
                    // Call the shared library pipeline
                    pipeline()
                }
            }
        }
    }
}
