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
               sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/DeclarativePipeline/webapp/target/webapp.war ubuntu@172.31.44.125:/home/test/webapps/testwebapp.war'
            }
        }




        
    }
    
    
}
