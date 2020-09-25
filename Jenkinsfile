pipeline {
    agent any
    stages {
        stage ("build"){
            steps {
                sh 'docker build --tag aurbnb:1.0 .'

                echo "done build \n"
            }
        }
        stage ("test"){
            steps {
                echo "testing \n"
            }
        }
        stage ("deploy"){
            steps {
                echo "deploying \n"
                sh 'docker run --publish 5000:5000 --detach --name arbnb aurbnb:1.0'
                echo "deployed \n"

            }
        }
    }
}