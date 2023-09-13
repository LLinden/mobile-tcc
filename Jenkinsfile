pipeline {
    agent any

    stages {
        stage('Clonar o repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/LLinden/teste-ebac-mobile.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'npm install'
            }
        }
        stage('Executar testes') {
            steps {
                sh 'NO_COLOR=1 npx wdio run ./wdio.conf.js'
            }
        }
    }
}