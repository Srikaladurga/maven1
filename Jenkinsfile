pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload-master')
        {
            steps
            {
                git 'https://github.com/intelliqittrainings/maven.git'
            }
        }
        stage('ContinuousBuild-master')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('ContinuousDeployment-master')
        {
            steps
            {
               deploy adapters: [tomcat9(credentialsId: 'bfb67f1d-2f4e-430c-bb8d-30584116bd00', path: '', url: 'http://172.31.51.212:9090')], contextPath: 'test1', war: '**/*.war'
            }
        }
  
    
    
    
}
