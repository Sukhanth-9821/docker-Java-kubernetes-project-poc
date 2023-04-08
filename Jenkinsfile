pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
            git branch: 'main', url: 'https://github.com/Sukhanth-9821/docker-Java-kubernetes-project-poc.git'
            }
        }
        stage ("maven build 1"){
            steps{
                sh 'cd productcatalogue'
                sh 'mvn clean install package'
            }
        }
        stage ("maven build 2"){
            steps{
                sh 'cd shopfront'
                sh 'mvn clean install package'
            }
        }
         stage ("maven build 3"){
            steps{
                sh 'cd stockmanager'
                sh 'mvn clean install package'
            }
        }
    }
}