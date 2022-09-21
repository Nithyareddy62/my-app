pipeline {
    agent any
    stages {
        stage('Git Checkout'){
            steps {
                git credentialsId:'MyGitHub',url: 'https://github.com/Nithyareddy62/my-app.git'
            }
        }
        stage('sonar qube'){
            steps {
                withSonarQubeEnv('sonarqube'){
                    sh 'mvn clean install sonar:sonar -DskipTests=true -Dsonar.organization="myapp" -Dsonar.projectKey="myapp-" -Dsonar.projectName="myapp-"'
                    sh '--illegal-access=warn'
                }
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests=true'
               
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package -DskipTests=true'
                
            }
        }
    }
}
