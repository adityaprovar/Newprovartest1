pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Get code from a GitHub repository
                git url: 'https://github.com/adityaprovar/sample_project.git', branch: 'master',
                 credentialsId: 'adityaprovar'
            }
        }
        stage('Test') {
            steps {
                  sh "pwd"
                  sh "ls"
                  bat 'ant -f sample_project/ANT/build.xml -Dtestproject.home=sample_project'
                
            }
        }
    }
}
