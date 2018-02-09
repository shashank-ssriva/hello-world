stage('Publish') {
			steps{
				xldPublishPackage serverCredentials: 'XLD720', darPath: 'build/libs/fileApp.dar'
			}
		}
		stage('Deploy') {
			steps{
				xldDeploy serverCredentials: 'XLD720', environmentId: 'Environments/LocalHost', packageId: 'Applications/DevOps/fileApp/${BRANCH_NAME}/${BUILD_NUMBER}'
			}
		}
