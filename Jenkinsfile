pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/PrajwalHajare/devopsdefaulter.git'
            }
        }

        stage('Build') {
            steps {
                sh 'javac Game.java'
                sh 'javac Main.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java Main'
            }
        }
    }
}
