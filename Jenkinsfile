pipeline{
    agent any
    stages{
        stage ('Build') {
            steps{
                echo "Build Success"
            }
        }
        stage('Deploy'){
            steps{
                deploy adapters: [tomcat8(credentialsId: 'a8b5e244-a45d-4728-80a9-dd4bc34f3b1d', 
                path: '', url: 'http://ec2-3-21-241-7.us-east-2.compute.amazonaws.com:8090/')], 
                contextPath: 'javawebapp', war: '**/java-web-project.war'
            }
        }
    }
}
