pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS612.cpp'
                sh 'g++ -o PES1UG20CS612 PES1UG20CS612.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS612'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploy Successful'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
