pipeline {
    agent any
     	
    stages {
                
        stage('Build') {
            steps {
                dir("my-app") {
                    sh 'mvn package'
                }
            }
        }
        stage('Deploy') {
            steps {
                dir("my-app/target"){
                sh 'sudo scp my-app-1.0-SNAPSHOT.jar atul@192.168.43.101:/home/atul'  
                }
            }
        }
    }
}
