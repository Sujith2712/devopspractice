pipeline {
   agent any
       stages {
        stage('test') {
            steps {
                sh 'echo hello'
            }
        }
           stage('test3') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'suji') {
                        echo 'I only execute on the master branch'
                    } else{
                        echo 'I execute on annother branch'
                    }
                }
            }
        }
        stage('test1') {
            steps {
                sh 'echo $TEST'
            }
        }
       
    }
}
