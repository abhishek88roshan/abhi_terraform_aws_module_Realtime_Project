@Library('shared_pipeline@main') _
pipeline {
    agent any

    stages {
        stage('Use Shared Pipeline') {
            steps {
                catchError(buildResult: 'FAILURE', stageResult: 'FAILURE') {
                    script {
                        echo "Debug: Attempting to call the shared pipeline"
                        pipeline()
                        echo "Debug: Shared pipeline executed"
                    }
                }
            }
        }
    }
}
