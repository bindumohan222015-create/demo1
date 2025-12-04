pipeline
{
    agent any
    
     environment {
   git_branch = "main"
   git_url = "https://github.com/bindumohan222015-create/demo1"
}
    stages 
    {
        stage('clone a project'){
            steps
            {
                git branch : "${git_branch}" , url : "${git_url}"
            }
        }
        stage('clean'){
            steps{
                sh 'mvn clean'
            }
        }
          stage('compile'){
            steps{
                sh 'mvn compile'
            }
        }
          stage('test'){
            steps{
                sh 'mvn test'
            }
        }
          stage('build'){
            steps{
                sh 'mvn clean install'
            }
        }
          stage('deploy'){
            steps{
                echo "deploy the project in to the webserver"
            }
        }
    }
}
