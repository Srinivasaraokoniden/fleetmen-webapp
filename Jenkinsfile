pipeline {
    agent any

    stages {

        stage('Checkout Repo') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Srinivasaraokoniden/fleetmen-webapp.git'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh '''
                
                kubectl apply -f Chapter9Deployments/

                '''
            }
        }
    }
}
