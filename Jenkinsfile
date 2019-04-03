pipeline {
    agent any
    stages {
        stage("PrintJob"){
            steps {
                script {
                    bat 'echo %JOB_NAME%' 
                }
            }
        }
    }
}
