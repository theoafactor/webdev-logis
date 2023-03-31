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

                        #perform some actions 
                        #make jenkins log into the ec2 account 
                        #give jenkins the permission to to able to carry out tasks on behalf of the ubuntu

                        ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/webkey.pem ubuntu@ec2-13-40-144-199.eu-west-2.compute.amazonaws.com 

                        apt update -y
                
                    '''
            }
        }
    }
}