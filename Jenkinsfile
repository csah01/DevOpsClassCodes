pipeline{
    tools{
        jdk 'jdk-11.0.1'
        maven 'maven3'
    }
    agent any
    stages{
        /*stage('checkout'){
            steps{
                git 'https://github.com/edureka-git/DevOpsClassCodes.git'
            }
        }*/
        stage('compile'){
            steps{
               bat 'mvn compile'
            }
        }
        stage('code review'){
            steps{
                bat 'mvn pmd:pmd'
            }
        }
        stage('Test '){
            steps{
                bat 'mvn test'
            }
        }
        /*stage('Metric Check '){
            steps{
                bat 'mvn cobertura:cobertura -Dcobertura.report.format=xml'
            }
        }*/
        stage('Package'){
            steps{
                bat 'mvn package'
            }
        }
    }
}
