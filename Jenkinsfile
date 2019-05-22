@Library('shared-lib2')_

node {
stage('build'){
    script {
        MUnit()
    }
}
stage('build') {
            script {
			sh 'mvn clean package'
         }
}
stage('Json coverage') {

  testFunc()
}
stage('MUnit Test Report') {
                script {
              publishHTML(target:[allowMissing: false,alwaysLinkToLastBuild: true,keepAll: true,reportDir: 'target/site/munit/coverage',reportFiles: 'summary.html',reportName: 'MUnit Test Report',reportTitles: 'MUnit Test Coverage Report'])
              }
              }
}
