pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh '''
                python3 -m venv venv
                source venv/bin/activate
                pip install -r requirements.txt
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                source venv/bin/activate
                nohup python3 app.py > app.log 2>&1 &
                '''
            }
        }

    }
}