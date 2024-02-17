pipeline {
    agent any
    tools {
        maven "MAVEN"
        jdk "OracleJDK8"
    }
    
    environment {
        SNAP_REPO = 'myapp-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'Soumya@1998'
		RELEASE_REPO = 'myapp-release'
		CENTRAL_REPO = 'myapp-central'
		NEXUSIP = '172.31.84.118'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'myapp-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
