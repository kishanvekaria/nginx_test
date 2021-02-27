pipeline{
    agent any
    options {
    skipStagesAfterUnstable()
    }
    
    stages{
        stage('Load balancer'){
            steps{
            sh "pwd"
            sh "ls -la"
            sh "scp /home/jenkins/.jenkins/workspace/jenkinsfirstpipeline/nginx.conf jenkins@35.197.94.79:nginx.conf"
           

            }
        }
    }
}
