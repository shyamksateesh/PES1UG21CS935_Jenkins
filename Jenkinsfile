pipeline{
    agent any{
        stages{
            stage('Build'){
                steps{
                    build 'PES1UG21CS935-1'
                    sh 'g++ main.cpp -o output'
                }
            }
            stage('Test'){
                steps{
                    sh './output'
                }
            }
            stage('Deploy'){
                steps{
                    echo 'Dployment Successful'
                }
            }
        }
        post {
            failure{
                echo 'Pipeline failed'
            }
        }
    }
}
