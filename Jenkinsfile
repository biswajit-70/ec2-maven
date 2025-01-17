pipeline {
     stages {
        stage('compile') {
		    agent{
			     node 'windows'    }
			tools{
			jdk 'JAVA_WIND'
			maven 'M2_WIND'
			}	 
          steps {
                git 'https://github.com/biswajit-70/ec2-maven.git'
			            	bat 'mvn compile'
            }
        }
		stage('package') {
		    agent{
			     node 'linux'    }
			tools{
			jdk 'JAVA_LIN'
			maven 'M2_LIN'
			}	 
            steps {
                git 'https://github.com/biswajit-70/ec2-maven.git'
	            			sh 'mvn compile'
            }
        }
    }
}
