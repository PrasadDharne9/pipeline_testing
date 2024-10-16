pipeline {
    agent any

    stages {
        stage('Run Python Script') {
            steps {
                script {
                    // Running the Python script directly
                    sh 'python Holt_Winters.py'
                }
            }
            post {
                success {
                    // Archiving artifacts only if the stage succeeds
                    archiveArtifacts artifacts: "**/*.xlsx", onlyIfSuccessful: true
                }
            }
        }
    }
}