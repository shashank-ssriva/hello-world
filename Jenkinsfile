node {
	stage('Publish') {
				xldPublishPackage serverCredentials: 'XLD720', darPath: 'build/libs/BridgeApp.dar'
			 }
	stage('Deploy') {
				xldDeploy serverCredentials: 'XLD720', environmentId: 'Environments/LocalHost', packageId: 'Applications/DevOps/BridgeApp/${BRANCH_NAME}/${BUILD_NUMBER}'
			 }
}
