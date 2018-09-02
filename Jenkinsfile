//Declarative//
pipeline{
   agent any
   stages{
      stage('build'){
	steps{
	   echo "Lets build Pet Clinic"
	   sh 'mvn clean install'
	}
      }
     stage('Test'){
      steps{
	 archiveArtifacts artifacts: "target/*.jar"
	 junit 'target/surefire-reports/*.xml'
      }
     }
  }
}
