pipeline{
  agent(label: 'master')
  tools(maven: 'M3')
  stages{
    stage('Checkout'){
      git branch: 'main', url: 'https://github.com/DoeschnerJan/SpringPetClinic.git'
    }
  }
}
