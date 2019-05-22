@Library('shared-lib2')_

pipeline{
    agent any
      stages{
          stage("Build"){
             steps{                
                    build {
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
                    
}
