pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS60xd2.cpp'
                sh 'g++ -o PES1UG20CS602 PES1UG20CS602.cpp'
                echo 'build stage success!!!'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS602'
                echo 'Test stage executed'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment Done'
            }
        }
    }
    post{
        failure{
            echo 'Failure in Pipeline'
        }
    }
}
