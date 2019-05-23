@Library('shared-lib2')_
import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import groovy.json.*
import java.net.URL
node {
  
  stage('build') {
            script {
			sh 'mvn clean package'
         }
}
  
