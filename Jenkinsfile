pipeline {
    agent any
    stages {
        stage("Check prevous jobs"){
            if (currentBuild?.getPreviousBuild()?.result == 'SUCCESS' ) {
                exit 1
            }
            if (currentBuild?.getPreviousBuild()?.getPreviousBuild().result == 'SUCCESS') {
                exit 1
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
