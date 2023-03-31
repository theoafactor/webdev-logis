pipeline{
    agent any
    stages {
        stage("test"){
            steps{
                sh '''
                        echo "welcome to the test"

                    '''
            }
        }


         stage("production"){
            steps{
                sh '''
                        echo "welcome to the production. Added Jenkins"
                        ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/webdev.pem ubuntu@ec2-18-170-115-158.eu-west-2.compute.amazonaws.com

                        sudo apt update -y

                        cd /var/www

                        sudo rm -rf html

                        git clone https://github.com/theoafactor/webdev-logis.git html

                        

                    '''
            }
        }

    }
}