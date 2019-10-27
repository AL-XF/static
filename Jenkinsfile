pipeline {
    agent any
    options {
        withAWS(credentials:'aws-static') 
    }
    stages {
        stage('Upload to AWS') {
            steps {
                tidy -q -e *.html
                s3Upload(file:'index.html', bucket:'jenkinsfxudacity', path:'index.html')
            }
        }
    }
}
