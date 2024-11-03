pipeline{
	agent any 
	stages{
		stage('1-git-clone'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkins_access', url: 'https://github.com/etech-technology/etech-exe']])
			}
		}
        stage('2-linuxcommand'){
            steps{
                sh 'uname -r'
            }
        }
		stage('3-compile'){
			steps{
				sh 'cat /etc/os-release'
			}
		}
        stage('4-disk-free'){
            steps{
                sh 'df -h'
            }
        }
	}
}