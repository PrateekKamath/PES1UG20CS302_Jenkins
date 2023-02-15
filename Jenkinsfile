pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o PNK_OP.cpp'
            }
        }
        stage('Test') { 
            steps {
                sh 'cat PNK_OP.cpp'
            }
        }
        stage('Deploy') { 
            steps {
                //sh './output'
                error 'Pipeline Failed' 
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
