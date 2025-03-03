# Jenkins pipeline for django project

pipeline {
    agent{
        label 'slave-1'
    }

    stages {
        stage('Code') {
            steps {
                echo "Cloning the code"
                git url: "https://github.com/PrasannaBiradar/django-notes-app.git", branch: "main"
            }
        }
        stage('Build'){
            steps{
                echo 'Building the code now'
                sh "whoami"
                sh "docker build -t notes-app:latest ."
            }
        }
        stage('DockerPush'){
            steps{
                echo "Push code to dockerhub"
                withCredentials([usernamePassword('credentialsId':"dockerhub-id",
                                                  usernameVariable:"dockerHubUser",
                                                  passwordVariable:"dockerHubPass")]){
                                                      sh "docker login -u ${env.dockerHubUser} -p ${dockerHubPass}"
                                                      sh "docker image tag notes-app:latest ${dockerHubUser}/notes-app:latest"
                                                      sh "docker push ${dockerHubUser}/notes-app:latest"
                                                  }
            }
        }
        stage('Deploy'){
            steps{
                echo "deploying the app"
                sh "docker run -d -p 8000:8000 prasanna616/notes-app:latest"
            }
        }
        
    }
}
