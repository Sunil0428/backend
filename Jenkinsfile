pipeline {
    agent any
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
                env.GIT_branch == 'main' // Executes this stage only on the 'main' branch
            }
            steps{
                sh 'echo this will execute only for main branch'
            }
        }
    }
}
