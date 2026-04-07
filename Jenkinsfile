pipeline{
  agent any

  tools{
    maven 'Maven'
  }

  stages{
    stage('checkout'){
      steps{
        git branch:'master', url:'https://github.com/nayangchawhan/mvn-last4'
      }
    }

    stage('build'){
      steps{
        sh 'mvn package'
      }
    }

    stage('compile'){
      steps{
        sh 'mvn compile'
      }
    }

    stage('test'){
      steps{
        sh 'mvn test'
      }
    }

    stage('run application'){
      steps{
        sh 'java -jar target/mvn-last4-1.0-SNAPSHOT.jar'
      }
    }
  }

  post{
    success{
      echo 'success'
    }
    failure{
      echo 'failure'
    }
  }
}
