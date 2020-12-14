pipeline {
   agent any
       stages {
        stage('build') {
            steps {
                sh "mvn clean install"
            }
        }
        stage('deploy') {
            steps {
                sh "cp -R /root/.jenkins/workspace/prac_pipeline1/target/* /opt/apache-tomcat-8.5.3/webapps"
            }
        }       
    }
}
