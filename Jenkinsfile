pipeline {
    agent any
   
    stages {
        stage('Build and deploying Docker image') 
        {
            steps {
                script {
                    sh """
                    echo "Building and deploying Docker image..."
                    ls -l
                    echo "Current directory contents listed."
                    echo "Building Docker image..."
                    sudo docker build -t my-app:latest .
                    sudo docker tag my-app:latest my-repo/my-app:latest
                    sudo docker run -d -p 8081:80 my-repo/my-app:latest

                    """
                    echo "Docker image built and deployed successfully."
                }
            
        }
    }
}
}