pipeline {
    agent { docker { image 'python:latest' } }
    stages {
        stage('build0') {
            steps {
                sh 'cd $HOME'
                sh 'echo $PWD'
                sh 'python --version'
            }
        }
        stage('build1') {
            steps {
                sh 'cd /Users/christopherbyrd/Projects/tf_aws_elasticsearch'
                sh 'echo $PWD'
                sh 'terraform --version'
            }
        }
        stage('build2') {
            steps {
                sh 'cd /Users/christopherbyrd/Projects/showme_code/codebase'
                sh 'echo $PWD'
                sh 'python -c 'print("register snapshot")''
            }
        }
        stage('build3') {
            steps {
                sh 'python -c 'print("delete existing indexes")''
            }
        }
        stage('build4') {
            steps {
                sh 'python -c 'print("restore snapshot")''
            }
        }
        stage('build5') {
            steps {
                sh 'python -c 'print("validate data accessibility")''
            }
        }
        
    }
}
