pipeline{
    agent any
    options {
    skipStagesAfterUnstable()
    }
    
    stages{
        stage('Load balancer'){
            steps{
            sh "ls -la"
            sh "pwd"
            sh "ssh -i ./ssh/id_rsa 35.222.180.87"
            sh "scp /home/jenkins/.jenkins/workspace/test_nginx/nginx.conf jenkins@35.222.180.87:nginx.conf"
            }
        }
    }
}
