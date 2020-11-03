pipeline
{
    agent {label'new-label'} 
     environment{
        PATH="/usr/share/maven:$PATH"
    }
    stages
    {
     
     stage ('compile code')
     {
         steps
         {
             sh 'mvn clean install'
         }
     }
     stage ('test')
     {
         steps
         {
             sh 'mvn test'
         }
     }
     stage ('find my binary')
     {
         steps
         {
             sh 'find / -name *.war'
         }
     }
     stage ('deploy')
     {
         steps
         {
             sh 'cp -R /root/.jenkins/workspace/pipeline2/target/* /opt/apache-tomcat-8.0.53/webapps'
         }
     }
        
    }
}
