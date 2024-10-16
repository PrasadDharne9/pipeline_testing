pipeline {
    agent any

    stages {
        stage('Activate Daikin Environment') {
            steps {
                sh 'C:/Users/DPrasad/Anaconda/condabin/activate C:/Users/DPrasad/Anaconda/envs/NeuralProphet'
            }                   
        }
        
        stage('Modeling') {
            steps {
                script {
                    sh "C:/Users/DPrasad/Anaconda/envs/NeuralProphet/python Hello_world.py"
                }
            }
            post {
                success {
                    archiveArtifacts artifacts: "**/*.xlsx", onlyIfSuccessful: true
                }
            }
        }
    
        stage('Deactivate Daikin Environment') {
            steps {
                sh 'C:/Users/DPrasad/Anaconda/condabin/deactivate C:/Users/DPrasad/Anaconda/envs/NeuralProphet'
            }
        }
    }
}