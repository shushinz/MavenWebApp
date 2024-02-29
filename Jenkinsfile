pipeline {
    agent any
    
    environment {
        PATH = "/usr/bin:$PATH" // Add /usr/bin to the beginning of the PATH
    }
    
    stages {
        stage('GetCode') {
            steps {
                git branch: 'main',
                url: 'https://github.com/shushinz/MavenWebApp.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
