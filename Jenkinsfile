node {
	stage('CreatePackage') {
				xldCreatePackage artifactsPath: 'BridgeApp', darPath: 'BridgeApp.dar', manifestPath: 'deployit-manifest.xml'
	}
	stage('Publish') {
				xldPublishPackage serverCredentials: 'XLD720', darPath: 'BridgeApp.dar'
			 }
	stage('Deploy') {
				xldDeploy serverCredentials: 'XLD720', environmentId: 'Environments/LocalHost', packageId: 'Applications/DevOps/BridgeApp/${BRANCH_NAME}/${BUILD_NUMBER}'
			 }
}
