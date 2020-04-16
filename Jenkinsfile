pipeline {

    agent any

     
    stages {
        
        stage ('checkout'){
            steps {
            git  https://github.com/Siddhartha-Rastogi/srinu.git'
            }
        }

        stage ('compile') {

            steps {

                withMaven(maven : '/opt/mvn/apache-maven-3.6.3') {

                    sh 'mvn clean compile'

                }

            }

        }

    



        stage ('test') {

            steps {

                withMaven(maven : '/opt/mvn/apache-maven-3.6.3') {

                    sh 'mvn test'

                }

            }

        }

        

        

        stage ('package') {

            steps {
                
                withMaven(maven : '/opt/mvn/apache-maven-3.6.3') {

                    sh 'mvn package'
                   

                }

            }

         }
        
        stage ('deploy') {
            
           
            steps {
                sh 'who am i'
                
                                withMaven(maven : '/opt/mvn/apache-maven-3.6.3') {

           sh 'cp /var/lib/jenkins/workspace/demopipe2/target/TomcatMavenApp-2.0.war /home/dineshreddy99077/noida/apache-tomcat-7.0.103/webapps/'
                
                sh 'mvn deploy'
               
            }
            }
            }
     
        

    }
}

