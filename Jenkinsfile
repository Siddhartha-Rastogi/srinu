pipeline {

    agent any

     
    stages {
        
        stage ('checkout'){
            steps {
            git  'https://github.com/Siddhartha-Rastogi/srinu.git'
            }
        }

        stage ('compile') {

            steps {



                    sh 'mvn clean compile'



            }

        }

    



        stage ('test') {

            steps {

          

                    sh 'mvn test'

         

            }

        }

        

        

        stage ('package') {

            steps {
                
 

                    sh 'mvn package'
                   



            }

         }
        
        stage ('deploy') {
            
           
            steps {
                sh 'who am i'
                
                   

           sh 'cp /var/lib/jenkins/workspace/demopipe2/target/TomcatMavenApp-2.0.war /home/dineshreddy99077/noida/apache-tomcat-7.0.103/webapps/'
                
                sh 'mvn deploy'
               
     
            }
            }
     
        

    }
}

