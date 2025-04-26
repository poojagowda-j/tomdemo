pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                 sh "rm -rf tomdemo"
               sh "git clone https://github.com/poojagowda-j/tomdemo.git"
            }
        }
        
        stage('build') {
            steps {
              sh "docker build -t hello-world:2.0 ."
            }
        }
        stage('push') {
            steps {
              sh "docker tag hello-world:2.0 poojagowda/my-repo:1.0"
              sh "docker login -u poojagowda -p 9845150490"
              sh "docker push poojagowda/my-repo:1.0"
            }
        }  
        stage('pull') {
            steps {
              sh "docker pull -t poojagowda/my-repo:1.0"
            }
        }
        stage('run') {
            steps {
              sh "docker run -d --name hello-world1 -P poojagowda/my-repo:1.0"
            }
        }
    }
}
