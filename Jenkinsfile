pipeline {
    agent any
    tools { 
        jdk 'JDK17' 
        maven 'Maven3' 
    }
    stages {
        stage('Build & Test') { 
            steps { 
                // Changed 'sh' to 'bat' because your Jenkins is on Windows
                bat 'mvn clean test' 
            } 
        }
    }
    post { 
        always { 
            // This stays the same; it looks for the XML results
            junit '**/target/surefire-reports/*.xml' 
        } 
    }
}
