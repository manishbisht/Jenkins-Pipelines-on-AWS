pipeline {
    agent any
    stages {
        stage('Lint HTML') {
            steps {
                sh 'tidy -q -e *.html'
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1', credentials:'aws-static') {
                    // do something
                    s3Upload(bucket:"jenkins-pipelines-on-aws", includePathPattern:'**/*');
                }
            }
        }
    }
}