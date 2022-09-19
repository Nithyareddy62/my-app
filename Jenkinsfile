pipeline {
    agent any
    stages {
    stage('Git Checkout'){
        steps{
            git credentialsId:'MyGitHub',url:'https://github.com/Nithyareddy62/my-app.git'

}
     }


      stage('Build') {
            steps {
                sh mvn clean install -DskipTests=true
            }
        }
        stage('Package') {
            steps {
                sh mvn package -DskipTests=true
            }
        }
    }
}
