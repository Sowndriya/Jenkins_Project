Pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Sowndriya/Jenkins_Project.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t img1 .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d --name ci-cd -p 5550:80 img1'
            }
        }
    }
}