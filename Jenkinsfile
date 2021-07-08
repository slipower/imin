pipeline {
    agent { label "linux"}
    stages {
        stage("build") {
            steps {
                sh """
                    docker build -t sebazzio/imin .
                """
            }
        }
        stage("run") {
            steps {
                sh """
                    docker run --rm -p 8081:80 sebazzio/imin
                """
            }
        }
    }
}