pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o output 1.cpp'
                build job: 'pes1ug20cs690-1'
            }
        }
        stage('Test') { 
            steps {
                sh './output'
            }
        }
        stage('Deploy') { 
            steps {
                echo "Success"
                //error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
