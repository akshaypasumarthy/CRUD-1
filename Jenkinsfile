pipeline{
    agent any
    tools {
        // Specify the Git executable
        git 'Git'
    }



    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'akshay', url: 'https://github.com/akshaypasumarthy/CRUD-1.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
