pipeline{
    agent any
    stages{
        stage("testing"){
            steps{
                sh '''echo This is the testing stage'''
            }
        }

        stage("prod"){
            steps{
                sh ''' echo This works fine

                        ### -- perform some actions

                        # 1. make jenkins log into the ec2 account 
                        ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/webkey.pem ubuntu@ec2-13-40-144-199.eu-west-2.compute.amazonaws.com 

                        # 2. update the packages
                        sudo apt update -y

                        # 3. grant jenkins permissions to the /var/www folder
                        # 4. get the project from github
                        cd /var/www
                        sudo rm -rf html
                        git clone https://github.com/theoafactor/webdev-logis.git html
                
                    '''
            }
        }
    }
}