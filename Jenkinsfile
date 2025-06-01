pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('a'){
			steps{
				git branch:'master',url:'https://github.com/rishitabafna/MyMavenWebApp2.git'
			}
		}
		stage('b'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('c'){
			steps{
				archiveArtifacts artifacts:'target/*.war', fingerprint=true
			}
		}
		stage('c'){
			steps{
				sh 'mvn clean package'
				sh 'ansible-playbook ansible/deploy.yml -i ansible/hosts.ini
			}
		}
	}
}
