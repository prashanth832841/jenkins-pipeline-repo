pipeline { 
    agent any 
    stages { 
       
        
        stage("Checkout") { 
            steps { 
                      git branch: "Main" ,   url : "https://github.com/devopsusergit/PetStoreWebApp.git"
                      sh  'mvn clean'
                      sh  ' mvn package'
            } 
        } 


        
        stage('Clean and Package') {
        steps {
        echo 'Cleaning workspace and packaging'
        sh 'mvn clean package'

        }

        }


        
        stage('Test Stage') {
        steps {
        echo 'Cleaning workspace and packaging'
        sh 'mvn clean package'

        }

        }
        



 
        stage('Parallel Stages') {
        parallel {
        stage('Code Quality Check') {
            steps{
            echo 'Running performance tests'
          }
         }
       stage('Performance test') {
         steps {
         echo 'Running code quality checks'
         }
        }
    
            
    stage('sequence'){
       stages{      
        stage('sequence stages'){
      
            stage('Regression Test') {
            steps{
            echo 'Running Regression tests'
            }
            }
                            
            
            stage('Acceptance Test') {
            steps{
            echo 'Running Acceptance tests'
            }
            }
               
                  }     
                  
                
            }
                
     }
}
        }



        
  }
}

                                                            






                                                       
