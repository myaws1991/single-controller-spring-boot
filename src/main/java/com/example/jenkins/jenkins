node('built-in')
{
   stage('ContinousDownload')
   {
     git 'https://github.com/myaws1991/single-controller-spring-boot.git'
   }
  stage('ContinousBuild')
   {
     sh 'mvn package'
   }
  stage('ContinousDeployment')
  {
     deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: '0316baca-cca4-4b5d-8303-743378548bdd', path: '', url: 'http://172.31.25.240:8080')], contextPath: 'testapp', war: 'target/*.war'
  }
}