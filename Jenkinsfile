stage('Run App') {
    steps {
        sh '''
        source venv/bin/activate
        nohup python3 app.py > app.log 2>&1 &
        '''
    }
}