pipeline {
    agent any
    stages {
        stage('Clonar Código') {
            steps { checkout scm }
        }
        stage('Ejecutar Pruebas Python') {
            steps {
                sh 'docker run --rm --volumes-from jenkins -w "$PWD" python:3.11-slim python -m unittest test_app.py'
            }
        }
    }
}
