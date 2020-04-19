pipeline {
	agent any
	stages {
		stage("Cleaning Stage") {
			steps {
				bat "mvn clean"
			}
		}
		stage("Testing Stage") {
			steps {
				bat "mvn test"
			}
		}
		stage("Packaging Stage") {
			steps {
				bat "mvn package"
			}
		}
		stage("Consolidate Results") {
			steps {
				input("Do you want to capture results?")
				junit'**/target/surefire-reports/TEST-*.xml'
				archive 'target/*.jar'
			}
		}
		//stage("Email Build Status") {
			//steps {
				//mail bcc: '', body: 'same as subject:)', cc: 'kingsley.erhigboboh@cognizant.com', from: '', replyTo: '', subject: 'cog-CRUD-jenkins-project-email-stage', to: 'kingsleyaerhi@gmail.com'
			//}
		//}
	}
}

	

				      
				
			
				
	

