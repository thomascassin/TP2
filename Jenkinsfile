pipeline{
	agent any
	stages {
		stage("1er etape: Nom de l etape"){
			steps{
			echo "Hello World"
			}
		}
		stage("2eme etape: Nom de l etape"){
			steps{
			echo "Hello World"
			}	
        }
        stage('Clone') {
         steps {
            checkout([$class: 'GitSCM',
                branches: [[name: '*/master' ]],
                extensions: scm.extensions,
                userRemoteConfigs: [[
                    url: 'https://github.com/SylvaineDidier/prrojet-for-training.git',
                    credentialsId: '86ebefd1-279b-46f1-be3a-ca3094b4750d'
                ]]
            ])

            //List all directories
            sh "ls -lart ./*"
            }
        }
        

		
	}
}