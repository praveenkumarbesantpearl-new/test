pipeline{
    agent any
    stages{
        stage("test"){
            when{
                changeset "tt"
            }
            steps{
                sh ("uname")
                echo "stage is sucess"
            }
        }
        stage("dev"){
            when{
                changeset "tt"
            }
            steps{
                sh("free")
                sh("df -h")
                echo "stage2 is sucess"
            }
        }
    }
    post{
        always{
            echo "Need to Build $BUILD_NUMBER IS SUCCESS OR NOT"
        }
        failure{
            echo "Build $BUILD_NUMBER is failed"
        }
        success{
            echo "Build $BUILD_NUMBER IS SUCCESS"
            sh("uname -r >/tmp/kern.txt")
        }
    }
}
