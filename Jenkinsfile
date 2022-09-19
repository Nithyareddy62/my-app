pipeline {
    agent any
    stages {
    

     


      stage('--Build--') {
            steps {
                sh "mvn clean install -DskipTests=true"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package -DskipTest=true"
            }
        }
    }
}
