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
        stage('Regression Acceptance Testing') {
        stages {
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


 stage('Testing') {
                   stage('Parallel Tasks') {
              parallel {
        stage('Performance Testing') {
            steps{
            echo 'Running performance tests'
          }
         }
       stage('Code Quality Check') {
         steps {
         echo 'Running code quality checks'
         }
        }
     }
}



        
  }
}

                                                            






                                                       
