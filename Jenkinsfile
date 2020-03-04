pipeline {
    /* agent { docker { image 'python:latest' } } */
    agent any
    stages {
        stage('build0') {
            steps {
                sh 'cd $HOME'
                sh 'echo $PWD'
                sh 'who am I'
            }
        }
        stage('build1') {
            steps {
                sh 'cd /Users/christopherbyrd/Projects/tf_aws_elasticsearch/'
                sh 'echo $PWD'
                sh 'terraform --version'
            }
        }
        stage('build2') {
            steps {
                sh 'cd /Users/christopherbyrd/Projects/showme_code/codebase'
                sh 'echo $PWD'
                sh 'python hello.py --count=3 --name=Chris'

            }
        }
        stage('build3') {
            steps {
                sh 'python hello.py --count=3 --name=Sally'
            }
        }
        stage('build4') {
            steps {
                sh 'python hello.py --count=3 --name=Mark'
            }
        }
        stage('build5') {
            steps {
                sh 'python hello.py --count=3 --name=Tom'
            }
        }
        
    }
}
