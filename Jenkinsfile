pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                git url: 'https://github.com/ShUbHaM25292003/JavaPipeline'
            }
        }
        
        stage('Compile') {
            steps {
                // Compile the Java code
                bat 'javac src/Main.java'
            }
        }
        
        stage('Run') {
            steps {
                // Run the Java program
                bat 'java -cp src Main'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        
        failure {
            echo 'Pipeline failed!'
        }
    }
}
