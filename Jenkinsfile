pipeline{
    agent any
    stages{
        stage("test"){
            steps{
                sh("uname")
                echo "test is sucess"
            }
        }
        stage("dev"){
            steps{
                sh("uptime >/tmp/up.txt")
                echo "dev is sucess"
            }
        }
        stage("prd"){
            steps{
                sh("free")
                echo "prd is sucess"
            }
        }
    }
            post{
            always{
                echo "need to ceck build is sucess or not"
            }
            failure{
                echo "build $BUILD_NUMBER IS FAILED"
            }
            success{
                echo "Build $BUILD_NUMBER IS SUCESS"
            }
        }
}
