#!groovy

node {
    stage('Checkout') {
        checkout scm
    }

    stage('Bundle') {
        sh "aws s3 sync --delete --acl public-read assets s3://${env.S3_CDN_BUCKET}/assets/"
    }
}
