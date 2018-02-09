//Initialising
node {
	stage('Publish') {
				xldPublishPackage serverCredentials: 'XLD720', darPath: 'build/libs/fileApp.dar'
			 }
	stage('Deploy') {
				xldDeploy serverCredentials: 'XLD720', environmentId: 'Environments/LocalHost', packageId: 'Applications/DevOps/fileApp/${BRANCH_NAME}/${BUILD_NUMBER}.0'
			 }
}
			
