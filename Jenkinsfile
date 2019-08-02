pipeline {
    agent any
    stages {
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