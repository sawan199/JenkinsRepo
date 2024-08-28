pipline{
    stages{
        stage("checkout code stage"){
            steps{
                git url:'https://github.com/sawan199/jenkinsRepo.git',branch:'main'

            }
        }
        stage("Build docker image"){
            steps{
                sh 'docker build -t myimage .'
            }
        }
        stage("create container"){
            step{
                sh 'docker run -d -p 8501:8501 myimage'
            }
        }
    }
}