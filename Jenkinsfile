pipeline {
    agent any

    stages {
        stage('Run Python Script') {
            steps {
                // Running the Python script directly
                sh 'python Hello_world.py'
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