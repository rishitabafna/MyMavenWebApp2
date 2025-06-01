pipeline{
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
	}
}
