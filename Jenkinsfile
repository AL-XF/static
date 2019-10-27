pipeline {
    agent any
    options {
        withAWS(credentials:'aws-static',region:'Oregon') 
    }
    stages {
        stage('Upload to AWS') {
            steps {
                s3Upload(file:'index.html', bucket:'jenkinsfxudacity', path:'index.html')
            }
        }
    }
}
