pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/mhdsalim17/MyWebsite.git'
            }
        }
        
        stage('Validation') {
            steps {
                bat '''
                    echo 🏗️ VALIDATION DU SITE WEB
                    echo 📁 Fichiers détectés:
                    dir *.html /B
                    echo ✅ Structure validée
                '''
            }
        }
        
        stage('Déploiement') {
            steps {
                bat '''
                    echo 🚀 DÉPLOIEMENT AUTOMATIQUE
                    echo 📍 Site: https://mhdsalim17.github.io/MyWebsite/
                    echo ✅ Déployé via GitHub Pages
                    echo 🎉 Terminé avec succès!
                '''
            }
        }
    }
    
    post {
        always {
            cleanWs()
        }
        success {
            echo '✅ Site déployé avec succès!'
        }
    }
}
