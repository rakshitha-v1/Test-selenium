pipeline{
  agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('checkout'){
      steps{
        git 'https://github.com/rakshitha-v1/Test-selenium.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn compile'
      }
    }
    stage('Test'){
      steps{
        sh 'mvn test'
      }
    }
    stage('Run Application'){
      steps{
        sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
      }
    }
  }
}
