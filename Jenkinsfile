pipeline {
    agent any
    stages {
        stage('Récupération du code') {
            steps {
                echo 'Clonage du repository...'
                git branch: 'main', url: 'https://github.com/Fvrenn/ci-cdTP.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Compilation / installation des dépendances...'
                sh 'echo "Build OK"'
            }
        }
        stage('Tests') {
            steps {
                echo 'Lancement des tests...'
                sh 'echo "Tests OK"'
            }
        }
    }
    post {
        success {
            echo 'Pipeline CI terminée avec succès !'
        }
        failure {
            echo 'Échec de la pipeline CI.'
        }
    }
}
