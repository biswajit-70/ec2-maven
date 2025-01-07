pipeline {
    tools{
        jdk 'JAVA_HOME'
        maven 'M2_SYST'
    }
    agent {
    node {
        label 'default'
         }
    }

    stages {
        stage('git cloning') {
            steps {
                git 'https://github.com/biswajit-70/ec2-maven.git'
                echo 'cloning successfully'
            }
        }
        
        stage('compiling'){
            steps{
                sh 'mvn compile'
                echo 'successfully compile'
            }
        }
        stage('testing'){
            steps{
                sh 'mvn test'
                echo 'successfully tested'
            }
        }
        stage('packaging'){
            steps{
                sh 'mvn package'
                echo 'sucessfully package'
            }
        }
    }
    post{
    success {
         junit '**/target/surefire-reports/TEST-*.xml'
         archiveArtifacts 'target/*.jar'
    }
    }
}
