pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Descargando código del repositorio...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Compilando el proyecto...'
                sh 'echo "Build completado"'
            }
        }

        stage('Test') {
            steps {
                echo 'Ejecutando pruebas...'
                sh 'echo "Pruebas ejecutadas correctamente"'
            }
        }

        stage('Deploy Simulation') {
            steps {
                echo 'Simulando despliegue...'
                sh 'echo "Aplicación desplegada (simulación)"'
            }
        }

    }
}