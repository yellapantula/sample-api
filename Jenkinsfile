@Library('shared-lib2')_

pipeline{
    agent any
      stages{
          stage("Build"){
             steps{                
                      always {
                        script {
                              cleanWs()
                              MUnit()
                          }
                      }            
                  
             }
          }
      }
                    
}
