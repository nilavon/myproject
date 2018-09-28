pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		sh "cd employees"
		sh "mvn clean install"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		sh "mvn clean test"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
		sh "mvn deploy"
            }
        }
    }
}