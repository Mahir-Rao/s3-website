pipeline {
    agent { label 'linux' }

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/Mahir-Rao/s3-website.git'
            }
        }

        stage('Deploy to S3') {
            steps {
                sh '''
                aws s3 sync . s3://appsmartz-project-website --delete
                '''
            }
        }
    }
}
