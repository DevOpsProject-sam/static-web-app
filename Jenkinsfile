pipeline {
    agent any
    
    stages {
        stage('Code Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/DevOpsProject-sam/static-web-app.git'
            }
        }
        stage('Continious Deploy') {
            steps {
                sh 'scp -i /home/ubuntu/AWSKEY.pem /project/static-web-app/* ubuntu@172.31.36.28:/var/www/html/'
            }
        }
    }
}
