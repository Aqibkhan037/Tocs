pipeline {
    agent any

    triggers {
        // Trigger the build whenever a change is pushed to the specified branch
        githubPush(branch: 'main')
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Aqibkhan037/Tocs.git', branch: 'main'
            }
        }
        
        stage('Run Python Script') {
            steps {
                sh 'gcloud compute zones list'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded! Python script executed.'
        }
        failure {
            echo 'Pipeline failed! Check your script and try again.'
        }
    }
}
