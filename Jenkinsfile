pipeline{
	agent{
		label 'slave1'
	}
	stages{
		stage('1-Clone'){
			steps{
				echo "This stage will run first"
			}
		}
		stage('2-Parallel Stage'){
			parallel{
				stage('1-subjob1'){
					agent{
						label 'slave2'
					}
					steps{
						echo "subjob1 running"
					}
				}
				stage('2-subjob2'){
					steps{
						echo "subjob2 running"
					}
				}
			}
		}
	}
}
