pipeline{
    agent any

    triggers {
        pollSCM('* * * * *')
    }
    stages{
        stage("Build"){
            steps{
                echo "Building the project"
                sh 'npm run build'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========Build executed successfully========"
                }
                failure{
                    echo "========Build creation failed========"
                }
            }
        }
    }
}