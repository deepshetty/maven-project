pipeline{
agent any
stages{
stage(-----clean-----){
step{
 sh "mvn clean"
}
}
stage(-----test-----){
step{
 sh "mvn test"
}
}
stage(-----package-----){
step{
 sh "mvn package"
}
}
}
}