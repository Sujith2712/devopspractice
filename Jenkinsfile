pipeline {
   agent any
   boolean MASTER_BRANCH=true

    stages {
        stage('test') {
            steps {
                sh 'echo hello'
            }
        }
        script{
            if (MASTER_BRANCH){
                sh 'echo master branch'
        }
            else{
                 sh 'echo   not master branch'
            }
        }
       
        stage('test1') {
            steps {
                sh 'echo $TEST'
            }
        }
    }
}
