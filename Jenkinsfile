pipeline{
    agent any
    stages{
        stage("pre"){
            when{
                changeset "praveen.yaml"
            }
            steps{
                sh("sudo yum install python3-pip* -y")
                echo "requirement 1 pip3 is installed"
            }
        }
        stage("pre2"){
            when{
                changeset "praveen.yaml"
            }
            steps{
                sh ("pip --version")
                echo "prerequest pip is installed"
            }
        }
        stage("pre3"){
            when{
                changeset "praveen.yaml"
                
            }
            steps{
                sh("sudo pip3 install ansible")
                echo "Ansible is sinatlled"
            }
        }
        stage("pre4"){
            when{
                changeset "praveen.yaml"
            }
            steps{
                sh("sudo ansible --version")
                echo "confirmed ansible ready"
            }
        }
    }

}
