@Library('shared-lib2')_
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
      JDK  'JAVA'
    	}
	stages {
	stage('build') {
            steps {
		        configFileProvider([configFile(fileId: 'config', variable: 'MAVEN_SETTINGS_XML')]) {
			sh "mvn -s $MAVEN_SETTINGS_XML clean package"
			}
	    }
	}
   }
}
  
