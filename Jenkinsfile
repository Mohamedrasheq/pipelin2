pipeline {
    agent any
    
    tools {
        // Use the Git tool installation configured in Jenkins
        git 'git'
    }
    
    stages {
        stage('Build') {
            steps {
                // Checkout the code from your Git repository
                git branch: 'main', url: 'https://github.com/Mohamedrasheq/pipelin2.git'
                
                // Build the Maven project
                bat 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                // Run Maven tests
                bat 'mvn test'
            }
        }
    }
}
