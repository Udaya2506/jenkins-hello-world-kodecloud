pipeline{
    agent any
    tools {
        maven 'Maven'
    }

    stages{
        stage("stage 1"){
            steps{
                echo "stage 1 executed "
                bat 'mvn -v'
               
            }
        }
        stage("git checkout "){
            steps{
                git branch: 'main', credentialsId: '9c407309-8c5e-4b42-b36c-f13848b4c9a3', url: 'https://github.com/Udaya2506/jenkins-hello-world-kodecloud.git'
                bat 'mvn clean package -DskipTests=true'
            }
        }
        stage("unit test"){
            steps{
                bat 'mvn test'
            }
        }

    }
}
