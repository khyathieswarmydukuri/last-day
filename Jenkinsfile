pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh'''
                zip -r index.html-$BUILD_NUMBER.zip *
                aws s3 cp index.html-$BUILD_NUMBER.zip s3://khyathieswar-vm/
                aws s3 cp s3://khyathieswar-vm/index.html-$BUILD_NUMBER.zip .
                unzip index.html-$BUILD_NUMBER.zip
                scp index.html root@44.211.193.215:/var/www/html/
                '''
            }
        }
    }
}


// git@github.com:khyathieswarmydukuri/last-day.git


// git@github.com:khyathieswarmydukuri/last-day.git