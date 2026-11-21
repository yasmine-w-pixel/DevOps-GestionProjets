pipeline {
    agent any

    tools {
        jdk 'jdk21'
        maven 'maven'
    }

    stages {
        stage('1 - Récupération du code') {
            steps {
                git branch: 'backend',
                    credentialsId: 'github-creds',
                    url: 'https://github.com/yasmine-w-pixel/DevOps-GestionProjets.git'
            }
        }

        stage('2 - Création du livrable') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
    }
}
