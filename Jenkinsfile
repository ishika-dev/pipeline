pipeline{
    agent any
    stages{
        stage("checkout the code"){
            steps{
                sh 'git clone https://github.com/Ramkhushi/java-code1.git'
            }
            
        }
        stage('move to javacod') {
            steps {
                sh 'cd ${WORKSPACE}/java-code1'
            }
        }
        stage('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('mvn test'){
            steps {
                sh 'mvn test'
            }
        }
        stage('Create a package'){
            steps {
                sh 'mvn package'
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
