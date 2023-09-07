pipeline {
    agent { label '' }
    

    environment {
        JAVA_HOME = "/usr/lib/jvm/java-11-openjdk-amd64"
        NEXUS_VERSION = "NEXUS3"
        NEXUS_PROTOCOL = "http"
        NEXUS_URL = "13.232.201.1:8081"
        NEXUS_REPOSITORY = "nexus"
        NEXUS_CREDENTIAL_ID = "Nexus"
    }

    stages {
        stage('Prepare') {
            
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            
            steps {

                sh 'export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64 && mvn verify package'
            }
        }

        stage('Unit Test') {
            
            steps {
                
                       sh 'export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64 && mvn test'
                   
               
            }
            
        }
        
        
     }
        
}
