node {
    stage('Preparation') { 
        git env.git_host        
    }
    stage('Build') {        
        sh './mvnw -Dmaven.test.failure.ignore verify'        
    }
    stage('Results') {
        junit '**/target/surefire-reports/TEST-*.xml'
        archiveArtifacts 'target/*.jar'       
    }
}
