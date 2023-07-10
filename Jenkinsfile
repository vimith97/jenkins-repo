pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'mvn clean compile'
                }
            
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'mvn test'
                }
            
        }


        stage ('Install Stage') {
            steps {
                
                    sh 'mvn install'
                }
            
        }
        
        stage ('Deploy Branch') {

            steps {
                    sh "mkdir /mnt/server/apache-tomcat-9.0.76/webapps/jenkins-game1"
                    sh "cp /root/.jenkins/workspace/multibranch-pipeline_master/target/jenkins-example-1.0-SNAPSHOT.jar /mnt/servers/apache-tomcat-9.0.76/webapps/jenkins-game1"

                }
            
        }
    }
}
