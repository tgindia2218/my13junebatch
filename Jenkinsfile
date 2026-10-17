pipeline{
	agent any;
	environment{
		a=300
		b=500
		git_token='git_pat983yt4893y983893535739857398'
		docker_token='docker_pat7135163513513517635135'
	}
	parameters{
		        choice(name: 'typeofbuild', choices: ['Release', 'Debug', 'Hotfix'], description: 'Type of build to execute')
				
				 string(name: 'packname', defaultValue: 'vsftpd', description: 'Who run this job ?')

	}
	triggers{
		pollSCM('* * * * *')
	}
	stages{
		stage("Hello wold this is Pink Color"){
			steps{
				echo "Hello world this is pink color"
				sh  'echo $a'
				sh  'echo $b'
			}
		}
		stage("Bbye world this is Black color"){
			steps{
				echo "Hello this is black "
				sh  'echo $a'
				sh  'echo $b'
		     	sh  "echo Env is ->  ${params.typeofbuild}"
				sh  "echo Requested package name is -> ${params.packname}"
				sh 'echo $git_token'
				sh 'chage -l jenkins'
				sh 'sudo chage -l jenkins'
				sh 'echo $docker_token'
				sh "sudo rpm -qa |  grep ${params.packname}"
				sh '''
						'whoami'
						'pwd'
						'cal'
						'id'
						'hostname'
						
				   '''
			}
		}
		stage("Welcome to Intersteller world"){
			steps{
				echo "Hello this is my world  "
				sh  'echo $a'
				sh  'echo $b'
  		     	        sh  "echo Env is ->  ${params.typeofbuild}"
				sh  "echo Requested package was is -> ${params.packname}"
				sh 'echo $git_token'
				sh 'echo $docker_token'				
				sh '''
						echo "Build Number --->  $BUILD_ID"
						echo "Project name --->  $JOB_NAME"
						echo "Workspace -->  $WORKSPACE"
						'hostname'
						'ifconfig'
				   '''
			}
		}
	}
}
