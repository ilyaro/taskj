pipeline {
    agent any
    stages {
        stage("PrintJob"){
            steps {
                script {
                    bat 'for /L %%a in (1,1,3) do (echo %JOB_NAME%) & if errorlevel 0 exit 0' 
                }
            }
        }
    }
}
