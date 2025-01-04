@Library('shared_pipeline@main') _
pipeline {
    agent any

    stages {
        stage('Use Shared Pipeline') {
            steps {
                catchError(buildResult: 'FAILURE', stageResult: 'FAILURE') {
                    script {
                        echo "Debug: Attempting to call the shared pipeline"
                        pipeline.func_from_module_1()
                        echo "Debug: Shared pipeline executed"
                    }
                }
            }
        }
    }
}
