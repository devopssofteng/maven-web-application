node{
    
    //def mavenHome = tool name: "maven-3.8.4"
    
    //properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '2', daysToKeepStr: '', numToKeepStr: '2')), pipelineTriggers([pollSCM('* * * * *')])])
    
    stage('CheckoutCode'){
      git branch: 'development', credentialsId: 'a9ba0cdd-997e-4402-8c6d-75ede8bf5b0e', url: 'https://github.com/devopssofteng/maven-web-application.git'
    }
    
    stage('Build'){
      sh "${mavenHome}/bin/mvn clean package"
    }
    
/*   
	  stage('UploadArtifactsIntoNexus'){
		  sh "${mavenHome}/bin/mvn deploy"
	  }

	
    stage('ExecuteSonarQubeReport'){
      sh "${mavenHome}/bin/mvn sonar:sonar"
    }
    
    stage('DeployAppIntoTomcatServer'){
        sshagent(['0800c4b5-efca-4642-84d6-97d622bd1b5d']) {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.110.191.194:/opt/apache-tomcat-9.0.64/webapps"
        }
    }
    
 */   
}
