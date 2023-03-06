pipeline{
    agent any

    stages{
        stage('Git Checkout'){
            steps{
                git branch: 'main', credentialsId: 'raji_git', url: 'https://github.com/rajeeb007/full-auto.git'
            }
        }
    }
}