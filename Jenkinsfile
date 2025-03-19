pipeline{
    agent any
    stages{
        stage('Clone repository'){
            steps {
                git url:"https://github.com/ancysnovee/new-repo.git",branch:"main"
            }

        }
        stage('build'){
            steps {
                echo 'building a project'
            }
        }
        stage ('test'){
            steps{
                echo 'running tests'
            }
        }
        stage ('deploy'){
            steps{
                echo 'deploying application'
            }
        }
    }
}
