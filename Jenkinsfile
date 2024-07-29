pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Kodları çekme
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                // Bağımlılıkları yükleme (Windows için bat komutu)
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                // Testleri çalıştırma (Windows için bat komutu)
                bat 'npm test'
            }
        }
        stage('Build') {
            steps {
                // Build işlemleri (Windows için bat komutu)
                bat 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                // Dağıtım işlemleri
                echo 'Deploying...'
            }
        }
    }
    
    post {
        always {
            // Temizlik işlemleri
            echo 'Cleaning up...'
        }
    }
}
