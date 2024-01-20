pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload')
        {
            steps
            {
                git branch: 'main', url: 'https://github.com/Devopsad4/mvn1.git'
            }
        }

        stage('ContinuousBuild')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('ContinuousDeployment')
        {
            steps
            {
               sh 'scp /home/ubuntu/.jenkins/workspace/Declartive/webapp/target/webapp.war ubuntu@172.31.44.125:/tmp/test/webapps/testwebapp.war'
            }
        }




        
    }
    
    
}
