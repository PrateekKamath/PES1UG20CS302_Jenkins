pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ PNK_OP.cpp -o Kamath' 
            }
        }
        stage('Test') { 
            steps {
                sh 'cat PNK_OP.cpp'
            }
        }
        stage('Deploy') { 
            steps {
                sh './Kamath'
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
