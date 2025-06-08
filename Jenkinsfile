

pipeline { 
    agent any 
    tools { 
        maven 'Maven' // Ensure name matches configured Maven installation 
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 'https://github.com/Nehal6669/g3.git'  
            } 
        } 
        stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
        } 
        stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
        } 
        stage('Run Application') {  
            steps { 
                bat 'java -jar app/build/libs app.jar'  
            } 
        } 
    } 
}
