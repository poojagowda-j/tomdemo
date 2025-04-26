pipeline {
    agent any
    stages {
        stage('pull') {
            steps {
              sh "docker pull -t poojagowdaj/hello-world:1.0.0"
            }
        }
        stage('run') {
            steps {
              sh "docker run -d --name hello-world1 -P poojagowdaj/hello-world:1.0.0"
            }
        }
    }
}
