pipeline {
    agent any
    stages {
        stage("Check prevous jobs"){
            steps{
                script{
                    if (currentBuild?.getPreviousBuild()?.result == 'SUCCESS' ) {
                        bat 'exit 1'
                    }
                    if (currentBuild?.getPreviousBuild()?.getPreviousBuild()?.result == 'SUCCESS' ) {
                        bat 'exit 1'
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
