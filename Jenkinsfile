pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Instalando dependencias...'
                bat 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Desplegando la aplicación...'
                bat 'npm start'
            }
        }
    }
}
