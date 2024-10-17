pipeline {
    agent any

    stages {
        stage('Activate Environment') {
            steps {
                bat '''
                    call C:\\Users\\DPrasad\\Anaconda\\Scripts\\activate.bat
                    call conda activate C:\\Users\\DPrasad\\Anaconda\\envs\\NeuralProphet
                '''
            }                   
        }
        
        stage('Code') {
            steps {
                script {
                    bat '''
                        C:\\Users\\DPrasad\\Anaconda\\envs\\NeuralProphet\\python Hello_world.py
                    '''
                }
            }
            post {
                success {
                    archiveArtifacts artifacts: "**/*.xlsx", onlyIfSuccessful: true
                }
            }
        }
    
        stage('Deactivate Environment') {
            steps {
                bat '''
                    call conda deactivate
                '''
            }
        }
    }
}