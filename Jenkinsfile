pipeline {
    agent any
    stages {
        stage('Build Angular') { steps { sh 'npm install && npm run build' } }
        stage('Deploy to S3') { steps { sh 'aws s3 sync dist/angular-app s3://your-angular-bucket --delete' } }
    }
}