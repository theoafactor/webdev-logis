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
                sh ''' echo This works fine'''
            }
        }
    }
}