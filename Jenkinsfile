pipeline {
    agent any

    stages {
        stage('Run Tests') {
            steps {
                sh 'git config --global --add safe.directory /var/jenkins_home/workspace/FirstTest'
                sh 'python3 -m pip install -r requirements.txt --break-system-packages'
                sh 'pytest --junit-xml=test_results.xml'
                junit 'test_results.xml'
            }
        }
    }
}
