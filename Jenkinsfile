pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	stages{
		stage('a'){
			steps{
				git branch:'master', url:'https://github.com/rishitabafna/MyGradleApp2.git'
			}
		}
		stage('b'){
			steps{
				sh 'gradle build'
			}
		}
		stage('c'){
			steps{
				sh 'gradle test'
			}
		}
		stage('d'){
			steps{
				sh 'gradle run'
			}
		}
	}
	post{
		success{
			echo 'Build successfully'
		}
		failure{
			echo 'BUild failed'
		}
	}
}
