pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Clonando el repositorio...'
                git 'https://github.com/JoseCQUADY/DevOps---API.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Instalando dependencias...'
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Desplegando la aplicación...'
                sh 'npm start'
            }
        }
    }
}
