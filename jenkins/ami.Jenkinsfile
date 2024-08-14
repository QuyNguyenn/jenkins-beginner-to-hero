pipeline {
	agent any

	parameters {
		string(name: "BUILD_VERSION", defaultValue: "", description: "The build version to be created AMI")
	}

	stages{
		stage("Build AMI") {
			steps {
				script {
					if (BUILD_VERSION == "") {
						echo "BUILD_VERSION is not specified."
						exit 1
					} else {
						echo "Create AMI from build version: ${BUILD_VERSION}"
					}
				}
			}
		}
		stage("Clean Up") {
			steps {
				echo "Clean Up"
			}
		}
	}
}