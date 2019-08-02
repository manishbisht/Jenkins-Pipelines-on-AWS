pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1') {
                    // do something
                    s3Upload(bucket:"jenkins-pipelines-on-aws", includePathPattern:'**/*');
                }
            }
        }
    }
}