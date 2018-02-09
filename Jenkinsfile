node {
	stage('Publish') {
				xldPublishPackage serverCredentials: 'XLD720', darPath: 'BridgeApp.dar', packageId: 'Applications/DevOps/BridgeApp/${BRANCH_NAME}/${BUILD_NUMBER}'
			 }
	stage('Deploy') {
				xldDeploy serverCredentials: 'XLD720', environmentId: 'Environments/LocalHost', packageId: 'Applications/DevOps/BridgeApp/${BRANCH_NAME}/${BUILD_NUMBER}'
			 }
}
