pipeline {
    agent any
    
    options {
        // Use predefined Git tool installation
        skipDefaultCheckout() // Skip the default checkout behavior
    }
    
    environment {
        // Define the Git tool installation to use
        GIT_HOME = tool 'git'
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
