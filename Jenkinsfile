@Library('shared-lib2')_
import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import groovy.json.*
import java.net.URL
node {

stage('Json coverage') {

  testFunc(MUnit)
}
stage('MUnit Test Report') {
                script {
              publishHTML(target:[allowMissing: false,alwaysLinkToLastBuild: true,keepAll: true,reportDir: 'target/site/munit/coverage',reportFiles: 'summary.html',reportName: 'MUnit Test Report',reportTitles: 'MUnit Test Coverage Report'])
              }
              }
}
