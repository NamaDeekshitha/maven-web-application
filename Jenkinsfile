node{
def maven = tool name: "maven3.8.4"
//checkout stage
stage('checkout'){
git branch: 'development', credentialsId: '67257a1b-7645-4426-9719-c9cac7b2b419', url: 'https://github.com/NamaDeekshitha/maven-web-application.git'
}

//build stage
stage('build'){
sh "$maven/bin/mvn clean package"
}
 /*
 //generate sonarqube report
stage('sonarqube'){
sh "$maven/bin/mvn sonar:sonar"
}
stage('nexus'){
sh "$maven/bin/mvn deploy"
}
stage('tomcat'){
    sshagent(['25754f72-8d15-4459-9851-25b860ffa82d']) {
        sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@15.206.90.152:/opt/apache-tomcat-9.0.59/webapps"
    // some block
}
}
*/
}//node closing
