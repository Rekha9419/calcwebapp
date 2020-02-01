node{
    stage('Cloning'){
        git 'https://github.com/Rekha9419/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
