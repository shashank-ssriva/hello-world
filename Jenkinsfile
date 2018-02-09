BRANCH DevOps
	stage('Publish') {
			agent{node {label 'master'}}
			steps{
				xldPublishPackage serverCredentials: 'XLD720', darPath: 'build/libs/fileApp.dar'
			}
		}
		stage('Deploy') {
			agent{node {label 'master'}}
			steps{
				xldDeploy serverCredentials: 'XLD720', environmentId: 'Environments/LocalHost', packageId: 'Applications/DevOps/fileApp/${BRANCH_NAME}/${BUILD_NUMBER}.0'
			}
		}
