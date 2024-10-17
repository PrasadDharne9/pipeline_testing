pipeline {
    agent any

    stages {
        stage('Activate Environment') {
            steps {
                echo 'Starting: Run Python Script'
                bat '''
                    call C:\\Users\\DPrasad\\Anaconda\\Scripts\\activate.bat
                    call conda activate C:\\Users\\DPrasad\\Anaconda\\envs\\NeuralProphet
                '''
            }                   
        }
        
        stage('Code') {
            steps {
                echo 'Starting: Run Python Script'
                script {
                    bat '''
                        C:\\Users\\DPrasad\\Anaconda\\envs\\NeuralProphet\\python Hello_world.py
                    '''
                }
                echo 'Python Script Executed'
            }
        }
    
    }
}