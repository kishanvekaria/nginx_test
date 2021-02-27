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
            sh "ssh -i ./ssh/id_rsa jenkins@35.197.94.79 docker run -d -p 80:80 --name nginx-loadbalancer --mount type=bind,source=/home/jenkins/nginx.conf,target=/etc/nginx/nginx.conf nginx:alpine"


            }
        }
    }
}
