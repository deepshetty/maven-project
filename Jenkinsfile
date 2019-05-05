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
step{
 sh "mvn package"
}
}
}
}