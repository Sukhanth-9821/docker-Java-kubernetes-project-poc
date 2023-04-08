pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('Checkout'){
            steps{
            git branch: 'main', url: 'https://github.com/Sukhanth-9821/docker-Java-kubernetes-project-poc.git'
            }
        }
        stage ("maven build 1"){
            steps{
                sh 'cd productcatalogue'
                sh 'mvn -f productcatalogue/pom.xml clean install package'
            }
        }
        stage ("maven build 2"){
            steps{
                sh 'cd shopfront'
                sh 'mvn -f shopfront/pom.xml clean install package'
            }
        }
         stage ("maven build 3"){
            steps{
                sh 'cd stockmanager'
                sh 'mvn -f stockmanager/pom.xml clean install package'
            }
        }
    }
}