pipeline {

     agent any
   
     stages {

           stage('Checkout') {
               steps{
                  checkout scm
               }
           }
           stage('Builder') {
               steps{
                sh '/home/mangesh/Software/apache-maven-3.6.1/bin/mvn install'
               }
           }
           stage('DeploymentD') {
              steps{
               sh 'sshpass -p "QAserver" scp target/Zala.war QAserver@172.17.0.2:/home/QAserver/Teast/apache-tomcat-8.5.43/webapps'
               
              }
           }

     }


}
