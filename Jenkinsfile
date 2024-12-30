@Library('shared_pipeline@main') _
pipeline {
    agent agent1

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
