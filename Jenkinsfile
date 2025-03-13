pipeline {
    agent any
    stages {
       // stage('Clone repository') {
          //  steps {
                // checkout([$class: 'GitSCM',
                // branches: [[name: '*/main']],
                // userRemoteConfigs: [[url: 'https://github.com/Srilakshmi-mothkur/PES1UG22CS608Jenkins.git']]])
            //}
        //}
        stage('Build') {
            steps {
                build 'PES1UG22CS608-1'
                sh 'g++ ./main/new.cpp -o new_exec'
                sh 'chmod +x new_exec'
            }
        }
        stage('Test') {
            steps {
                sh './ew_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
