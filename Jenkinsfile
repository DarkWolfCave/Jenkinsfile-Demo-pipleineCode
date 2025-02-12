pipeline{
agent any
tools{
maven 'mymaven'
}
stages{
stage('Parallel Stages'){
   parallel{
   stage('test on windows'){
   // agent {win_server}
   steps{
    git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
    sh 'mvn test'
   }
   }
   stage('test on Mac'){
   // agent {mac_server}
   steps{
    git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
    sh 'mvn test'
   }
   }
   }
}
}
}
