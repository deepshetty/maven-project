pipeline{
agent any
stages{
stage('-----clean-----'){
steps{
 sh "mvn clean"
}
}
stage('-----test-----'){
steps{
 sh "mvn test"
}
}
stage('-----package-----'){
steps{
 sh "mvn package"
}
}

stage('-----deploy-----'){
sshagent(['tomcat']) {
   sh 'scp -o StrictHostKeyChecking=no target/*.war tomcat@3.18.104.251:opt/tomcat8/webapps'
}
}

}
}