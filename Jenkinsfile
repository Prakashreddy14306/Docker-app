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
                    docker build -t my-app:latest .
                    docker tag my-app:latest my-repo/my-app:latest
                    docker run -d -p 8082:80 my-repo/my-app:latest

                    """
                    echo "Docker image built and deployed successfully."
                }
            
        }
    }
}
}