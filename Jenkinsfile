pipeline {
    agent { label 'Agent-1' }
    stages{
        stage("Initial")
        {
            steps{
                sh 'echo this is my first jenkins job'
            }
        }
        stage ("second stage")
        {
            steps{
                sh 'echo this is the second stage of the job'
            }
        }
        stage ("test stage")
        {
            when {
            expression { env.BRANCH_NAME == 'origin/main' }
            }
            steps{
                sh 'echo this will execute only for hello world branch'
            }
        }
    }
}
