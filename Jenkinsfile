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
    	}
	stages{
	  stage('build') {
		  steps{
		    script {
				sh 'mvn clean package'
		 	   }
		  }
			}
	}
}
  
