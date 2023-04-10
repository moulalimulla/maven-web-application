node{
    def mavenHome = tool name: "Maven 3.9.1"
   // properties([pipelineTriggers([pollSCM('* * * * *')])])
stage('checkout')
{
    git branch: 'development', credentialsId: '925b84b3-94c7-41cf-8ff7-3b8bf8258841', url: 'https://github.com/moulalimulla/maven-web-application.git'
}
stage('Build')
{
    sh "${mavenHome}/bin/mvn clean package"
}
// stage('sonarqubeexecutereport')
// {
//     sh "${mavenHome}/bin/mvn sonar:sonar"
// }
// stage('uploadartifactintonexus')
// {
//     sh "${mavenHome}/bin/mvn deploy"
// }
// stage('Deployartifactintotomcat')
// sshagent(['5dc6a685-d0d0-4bd1-8241-c472a686ca7c']) 
// {
// sh "scp -o StrictHostkeyChecking=no target/maven-web-application.war ubuntu@65.0.86.25:/opt/tomcat/webapps/"
// }
// stage('Mail')
// {
//     mail bcc: '', body: 'Sucess', cc: '', from: '', replyTo: '', subject: 'Pipeline', to: 'ms.moulali2159@gmail.com'
// }
}
