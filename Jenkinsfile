pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    echo 'Construyendo la imagen Docker...'
                    sh 'docker build -t sicei-app .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    echo 'Ejecutando el contenedor Docker...'
                    bat 'docker run -d -p 3000:3000 sicei-app'
                }
            }
        }

        stage('Clean Up') {
            steps {
                script {
                    echo 'Limpiando contenedores y imágenes...'
                    bat 'docker rm -f $(docker ps -aq)' 
                    bat 'docker rmi -f sicei-app'
                }
            }
        }
    }
}
