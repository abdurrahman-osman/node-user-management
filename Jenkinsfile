pipeline {
    agent any
    
    environment {
        // Gerekli çevresel değişkenler
        NODE_HOME = '/usr/local/bin/node'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Kodları çekme
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                // Bağımlılıkları yükleme
                script {
                    sh 'npm install'
                }
            }
        }
        stage('Test') {
            steps {
                // Testleri çalıştırma
                script {
                    sh 'npm test'
                }
            }
        }
        stage('Build') {
            steps {
                // Build işlemleri
                script {
                    sh 'npm run build'
                }
            }
        }
        stage('Deploy') {
            steps {
                // Dağıtım işlemleri (bu örnekte yer almıyor, ihtiyaca göre ekleyin)
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
