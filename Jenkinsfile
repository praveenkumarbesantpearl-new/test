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
        stage("copying index"){
            when{
                changeset "praveen.yaml"
            }
            steps{
                sh ("sudo cp /tmp/index.html /var/www/html")
            }
        }
        stage("copyig the yaml file"){
            when{
                changeset "praveen.yaml"
            }
            steps{
                sh ("sudo cp $WORKSPACE/praveen.yaml /tmp")
            }
        }
        stage ("Running playbook"){
            when{
                changeset "praveen.yaml"
            }
            steps{
                sh ("sudo ansible-playbook /tmp/praveen.yaml")
            }
        }
    }

}
