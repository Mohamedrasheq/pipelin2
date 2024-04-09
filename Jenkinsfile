pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Ensure Git is properly configured
                // Specify the path to the Git executable
                tool 'git'
                
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
