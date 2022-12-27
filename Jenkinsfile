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
        stage('integration testing'){

        steps{
                sh 'mvn verify -DskipUnitTests'
        }
        }
        stage('Maven Build'){

        steps{
                sh 'mvn clean install'
        }
        }
        stage('static code analysis'){

        steps{
            script{withSonarQubeEnv(credentialsId: 'sonar-api') {
                    sh "mvn clean package sonar:sonarS"
    // some block
}}
                
        }
        }
    }
}