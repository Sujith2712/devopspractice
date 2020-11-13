pipeline{
    agent any
    environment{
        PATH="/usr/share/maven:$PATH"
    }
   stages {
    stage ('pulling code from github')
    {
        steps{
          git credentialsId: 'pipeline12', url: 'https://github.com/RavitejaAdepudi/javawar.git'
        }
        
        }
        stage ('build')
        {
        steps {
            sh 'mvn clean install'
        }
    }
       stage ('test')
        {
        steps {
            sh 'mvn test'
        }
    }
}
}
