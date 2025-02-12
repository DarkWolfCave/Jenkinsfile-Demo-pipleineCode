pipeline{

agent any  // any = any available server(current lab server) where jenkisn can run the pipleine

tools{
  maven 'mymaven'
}
stages{
stage('Checkout Code'){
  steps{
     git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
  }

}
stage('CompileCode'){
steps{
  sh 'mvn compile'
}
}

stage('Review Code'){
steps{
  sh 'mvn pmd:pmd'
}
}

stage('Test Code'){
steps{
  sh 'mvn test'
}
}

stage('Build Code'){
steps{
  sh 'mvn package'
}
}

}
}
