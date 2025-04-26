pipeline {
    agent any
    stages {
        stage('pull') {
            steps {
              sh "docker pull poojagowdaj/hello-world"
            }
        }
        stage('run') {
            steps {
              sh "docker run -d --name hello-world1 -p 8090:8080 poojagowdaj/hello-world:1.0.0"
            }
        }
    }
}
