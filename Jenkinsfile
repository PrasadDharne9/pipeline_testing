pipeline {
    agent any

    stages {
        stage('Activate Environment') {
            steps {
                echo 'Starting: Run Python Script'
                bat '''
                    call conda activate D:\\Users\\Prasad.Dharne\\AppData\\Local\\miniconda3\\envs\\strettoforecast
                '''
            }                   
        }
        
        stage('Code') {
            steps {
                echo 'Starting: Run Python Script'
                script {
                    bat '''
                        D:\\Users\\Prasad.Dharne\\AppData\\Local\\miniconda3\\envs\\strettoforecast\\python Hello_world.py
                    '''
                }
                echo 'Python Script Executed'
            }
        }
    
    }
}