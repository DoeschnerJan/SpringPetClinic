declarative pipeline example:
pipeline{
  agent(label 'master')
  tools(maven 'M3')
  stages{
    stage('Checkout'){
        git branch: 'main', url: 'https://github.com/DoeschnerJan/SpringPetClinic.git'
    }	
	stage('Build'){
        withMaven(maven: 'M3'){
            sh 'mvn compile'
        }
    }
	stage('Test'){
        withMaven(maven: 'M3'){
            sh 'mvn test'
        }
    }
	stage('Package'){
        withMaven(maven: 'M3'){
            sh 'mvn package'
        }
    }
	stage('Deploy'){
        withMaven(maven: 'M3'){
            sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
        }
    }
  }
}
