pipeline{
    agent any
    stages{
        stage('Clone repository'){
            steps {
                git url:"https://github.com/ancysnovee/new-repo.git",branch:"main"
            }

        }
        stage('Dependency'){
            steps {
                echo 'installing dependencies'
                bat '''
                    python -m venv venv
                    call venv\\Scripts\\activate
                    python -m pip install --upgrade pip
                    pip install -r requirements.txt
                    '''
            }
        }
        stage ('test'){
            steps{
                echo 'running tests'
                bat '''
                    call venv\\Scripts\\activate
                    pytest test.py
                    '''
                    
            }
        }
        stage ('deploy'){
            steps{
                echo 'deploying application'
                bat '''
                    call venv\\Scripts\\activate
                    python hello.py
                    '''

            }
        }
    }
}
