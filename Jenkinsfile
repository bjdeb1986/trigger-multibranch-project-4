pipeline{
    agent{
        node{
            label 'agent01'
        }
    }
    options{
        buildDiscarder(logRotator(numToKeepStr: '5'))
        disableResume()
        disableConcurrentBuilds()
        timestamps()
    }
    stages{
        stage('Build'){
            steps{
                sh 'sleep 2'
                sh 'cat /etc/os-release'
            }
        }
        stage('Test'){
            steps{
        	sh 'sleep 2'
		sh 'uptime'
            }
        }
    }
    post{
	cleanup{
		echo "Workspace cleanup"
		cleanWs()
	}
    }
}
