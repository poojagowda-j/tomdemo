pipeline {
  agent { label 'slave1' }
         stages {
           stage('Checkout') {
             steps {
               sh "rm -rf tomdemo"
               sh "git clone https://github.com/poojagowda-j/tomdemo.git"
             }
           }
           stage('build') {
             steps {
               sh "cd tomdemo"
               sh "mvn clean package"
             }
           }
           stages('deploy') {
             steps {
               sh "scp target/*.war /opt/apache-tomcat-11.0.3/webapps"
             }
           }
         }
        }
          
               sh "git
