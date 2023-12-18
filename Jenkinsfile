pipeline {
    agent any
    
    stages {
        stage('Code Checkout') {
            steps {
                git 'https://github.com/DevOpsProject-sam/static-web-app.git'
            }
        }
        stage('Continious Deploy') {
            steps {
                sh 'scp -i /home/ubuntu/AWSKEY.pem /project/static-web-app/* ubuntu@172.31.27.2:/var/www/html/'
            }
        }
    }
}
