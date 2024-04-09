pipeline {
    agent any
    
    options {
        // Use predefined Git tool installation
        tools {
            // Specify the name of the Git tool installation configured in Jenkins
            git 'git'
        }
    }
    
    stages {
        stage('Build') {
            steps {
                // Checkout the code from your Git repository
                git 'https://github.com/Mohamedrasheq/pipelin2.git'
                
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
