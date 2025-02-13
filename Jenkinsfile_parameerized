pipeline{

agent any

tools{
  maven 'mymaven'
}

parameters{
      
       choice(name: "ENV",choices: ["","Dev","QA"])

}

stages{

    stage('Build on Dev Server')
     {
         when{
          expression{ params.ENV == 'Dev' }
         }
         steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
                sh 'mvn compile'

             }

          }

      stage('Build on QA Server')
     {
         when{
          expression{ params.ENV == 'QA' }
         }
         steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
                sh 'mvn test'

             }

          }

}

}
