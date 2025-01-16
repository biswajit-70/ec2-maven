pipeline{
stages{
stage{
tools{
jdk 'JAVA_HOME'
maven 'M2_SYST'
}
agent{
label'default'
}
steps{
 git 'https://github.com/biswajit-70/ec2-maven.git'
 sh 'mvn compile'

}
}

}
}
