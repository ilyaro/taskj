pipeline {
    agent any
    stages {
        stage("Check prevous jobs"){
            steps{
                script{
                    if (currentBuild?.getPreviousBuild()?.result == 'SUCCESS' ) {
                        exit 1
                    }
                }
            }
        }
        stage("PrintJob"){
            steps {
                script {
                   bat 'echo %JOB_NAME%' 
                }
            }
        }
    }
}
