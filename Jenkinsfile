pipeline{
    agent{
        dockerfile true
    }
    stages{
        stage("Test"){
            steps{
                echo "========executing A========"
                sh 'node --version'
                sh 'svn --version'
                sh 'hostname'
                sh 'pwd'
                sh 'ls -altr'
                sh 'printenv'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
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