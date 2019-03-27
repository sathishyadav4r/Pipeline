node  {
			stage('SCM')  {
				// git clone
				git 'https://github.com/sathish4r/spring-petclinic.git'
				}
				
			stage('build the packages')  {
				// mvn package
				sh 'mvn package'
				}

			stage('SonarQube analysis') {
				withSonarQubeEnv('Sonar-6.4') {
			// requires SonarQube Scanner for Maven 3.2+
				sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'
   				 }
  			}	
}	  