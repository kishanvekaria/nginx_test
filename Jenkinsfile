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
            sh "scp /home/jenkins/.jenkins/workspace/test_nginx/nginx.conf jenkins@35.222.180.87:nginx.conf"
            sh "ssh -i ./ssh/id_rsa jenkins@35.222.180.87  && docker run -d -p 80:80 --name nginx-loadbalancer --mount type=bind,source=/home/jenkins/nginx.conf,target=/etc/nginx/nginx.conf nginx:alpine"

            }
        }
    }
}
