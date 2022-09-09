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
                    url: 'https://github.com/thomascassin/TP2.git',
                    credentialsId: '7d77f428-1aaa-4c9d-9bdf-075f9fbcfae1'
                ]]
            ])

            //List all directories
            sh "ls -lart ./*"
            }
        }
        

		
	}
}