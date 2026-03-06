pipeline{
    agent any
    stages{
        stage("test"){
            when{
                changeset "tt"
            }
            steps{
                sh("uname")
                echo "test is sucess"
            }
        }
        stage("dev"){
            when{
                changeset "tt"
            }
            steps{
                sh("uptime >/tmp/up.txt")
                echo "dev is sucess"
            }
        }
        stage("prd"){
            when{
                changeset "tt"
            }
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
