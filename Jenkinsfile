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
        script {
          echo 'This is for stage 3 assessment.'
        }
      }
    }
    
        
        stage('Parallel Stages ') {
        parallel {
        
        stage('Code Quality Check') {
        steps{
            echo 'Running Quality tests'
          }
         }
            
       stage('Performance Test') {
         steps {
         echo 'Running Performance checks'
         }
        }
            
        stage('Sequence'){
         stages{          
        stage('Regression Testing') {
        steps {
        echo 'Running regression tests'
       }
      }
             
     stage('Acceptance Testing') {
        steps {
        echo 'Running acceptance tests'
       }
      }
     
         
    }
    }  
    }
    }
}
}

                                                            






                                                       
