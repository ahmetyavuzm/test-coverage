@Library('aus-pipeline-lib') _

pipeline {
    agent any

    options {
        timestamps()
    }

    stages {
        stage('Test & Coverage') {
            steps {
                echo '🚀 Running test coverage pipeline...'
                runTestCoveragePipeline()
            }
        }
    }

    post {
        success {
            echo '✅ Coverage pipeline completed successfully.'
        }
        failure {
            echo '❌ Pipeline failed.'
        }
    }
}
