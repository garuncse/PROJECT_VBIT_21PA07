pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                echo 'Cloning Repository...'
                git 'https://github.com/garuncse/PROJECT_VBIT_21PA07.git'
            }
        }

        stage('Compile Java File') {
            steps {
                echo 'Compiling Java File...'
                sh 'javac Test.java'
            }
        }

        stage('Execute Java File') {
            steps {
                echo 'Running Java File...'
                sh 'java Test'
            }
        }
    }

    post {
        success {
            echo 'Java file executed successfully!'
        }
        failure {
            echo 'Build failed! Check console output.'
        }
    }
}
