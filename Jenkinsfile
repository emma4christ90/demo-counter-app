pipeline{

    agent any

    stages{

        stage('Git Checkout'){

        steps{
                git branch: 'main', url: 'https://github.com/emma4christ90/demo-counter-app.git'
        }
        }
        stage('UNIT Testing'){

        steps{
                sh 'mvn test'
        }
        }
    }
}