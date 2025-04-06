pipeline {
    agent any

    stages {
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
