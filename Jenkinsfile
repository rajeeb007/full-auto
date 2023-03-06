pipeline{
    agent any

    stages{
        stage('Git Checkout'){
            steps{
                git branch: 'main', credentialsId: 'raji_git', url: 'https://github.com/rajeeb007/full-auto.git'
            }
        }
        stage('UNIT Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('mvn build'){
            steps{
                sh 'mvn clean install'
            }
        }
        stage('sonar qulaity check'){
            steps{
                script{
                    withSonarQubeEnv(installationName:'sonarqube ', credentialsId:'sonarkey') {
                    sh 'mvn sonar:sonar'
                 }
                }
                
            }
        }
    }
}