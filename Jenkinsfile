pipeline{
agent any

tools{
maven 'mymaven'
}

stages{
    

stage('Build Code')
{
  steps{
        git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
        sh 'mvn package'
        script{
          timeout(time: 10,unit: 'MINIUTES'){
          input(id: 'DeplpoyCode',message: 'Continue Deploy stage',ok: 'Deploy')
       }
    }
 
  }

}

stage('Deploy Code')
{

 steps{
        echo "Deployment Completed"
 }
}

}
}
