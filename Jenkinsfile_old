pipeline{
    agent any
    stages{
        stage("test"){
            when{
                changeset "uuu"
            }
            steps{
                echo "step1 is sucess"
            }
            
        }
        stage("test2"){
            when{
                changeset "uuu"
            }
            steps{
                echo "step2 is sucess"
            }
        }
        stage("test3"){
            when{
                anyOf{
                    changeset "uuu"
                    changeset "ttt"
                }
            }
            steps{
                echo "test is success"
            }
        }
    }
    post{
        always{
            echo "Should even if its sucess or failure"
        }
        success{
            echo "build is success"
        }
        failure{
            echo "Build is failure"
        }
    }
}
