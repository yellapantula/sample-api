@Library('shared-lib2') _
import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import groovy.json.*
import java.net.URL
pipeline{
  agent any
    tools {
      maven 'Maven'
      jdk  'JAVA'
    	}
	stages {
		stage('build') {
		    steps {
				configFileProvider([configFile(fileId: 'config', variable: 'MAVEN_SETTINGS_XML')]) {
				sh "mvn -s $MAVEN_SETTINGS_XML clean package"
				}
		    }
		}
		stage('test function'){
			steps{
				script{
				testFunc()
				}
			}
		}

		stage('MUnit Test Report') {
		       steps{
				script {
			      publishHTML(target:[allowMissing: false,alwaysLinkToLastBuild: true,keepAll: true,reportDir: 'target/site/munit/coverage',reportFiles: 'summary.html',reportName: 'MUnit Test Report',reportTitles: 'MUnit Test Coverage Report'])
				}
			      }
			}	
	}





   	
	
}
  
