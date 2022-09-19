pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
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
