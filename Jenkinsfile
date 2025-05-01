pipeline {
    agent any

    tools {
        maven 'Maven 3.9.6' // Jenkins’te tanımladığın Maven adıyla birebir aynı olmalı
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/sedabayog/hello-jenkins.git' // kendi GitHub adresinle değiştir
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
