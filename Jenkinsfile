pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Aqibkhan037/Tocs.git', branch: 'main'
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'Python.py'
            }
        }
    }
}
