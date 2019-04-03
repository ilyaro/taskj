pipeline {
    agent any
    stages {
        stage("PrintJob"){
            steps {
                script {
                    currentBuild.displayName = "The name."
                    currentBuild.description = "The best description."
                }
            }
        }
    }
}
