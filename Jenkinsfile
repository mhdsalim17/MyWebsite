pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']], // ou '*/master' selon votre branche
                    extensions: [],
                    userRemoteConfigs: [[url: 'https://github.com/mhdsalim17/MyWebsite.git']]
                ])
            }
        }
        
        stage('Validation') {
            steps {
                // Vos étapes de validation
            }
        }
        
        stage('Déploiement') {
            steps {
                // Vos étapes de déploiement
            }
        }
    }
    
    post {
        always {
            cleanWs()
        }
    }
}
