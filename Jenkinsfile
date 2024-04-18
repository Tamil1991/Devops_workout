pipeline {
    agent any

    stages {
        stage('cloning process') {
            steps {
                sh 'rm -rf Devops_workout'
                echo 'Cloning the repo'
                sh 'git clone https://github.com/Tamil1991/Devops_workout.git'
            }
        }
        stage('Running python server') {
            steps {
                echo 'Running python server on port 8000'
                sh 'cd Devops_workout'
                sh 'export JENKINS_NODE_COOKIE=dontKillMe;export BUILD_ID=dontKillMe; nohup /usr/bin/python3 -m http.server &'
            }
        }
    }
}
