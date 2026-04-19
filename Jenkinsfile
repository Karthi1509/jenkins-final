pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                pkill -f app.py || true
                nohup python3 app.py > output.log 2>&1 &
                '''
            }
        }
    }
}