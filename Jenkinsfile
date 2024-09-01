pipeline {
    agent any 
    stages {
        stage ('checkout') {
            steps {
                git branch: 'develop', url: 'https://github.com/mkranthi/kubernetes.git'
            }
        }
        stage('build image from Dockerfile') {
            steps {
                sh 'docker build -t practice-imageversion1 .'
            }
        }
        stage('tag the image') {
            steps {
<<<<<<< HEAD:jenkinsfile
                sh 'docker tag practice-imageversion1 kmannedev/practice-imageversion1:v1.0'
            }
        }
        stage('push the image') {
            steps {
                sh 'docker push kmannedev/practice-imageversion1:v1.0'
=======
                sh 'docker tag practice-imageversion1 kmannedev/practice-imageversion1:v1.0'
>>>>>>> 543cec57ca5dfa26d8abc0ddf2e4296438cdf4ca:Jenkinsfile
            }
        }
        stage('kubectl ') {
            steps {
                sh 'kubectl create -f deployment.yaml'
            }
        }
    }
}
