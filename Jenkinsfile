node {
    
    stage('Gitclone') {
	   git branch: 'main', credentialsId: 'f5bd9ca4-14b1-45d4-971d-ec7d0db94de2', url: 'https://github.com/rithvikpreethireddy/jenkinspro22.git'
       
    }
	stage('java version') {
	      
           sh 'java -version'
    }
	stage('maven version') {
	       
          sh 'mvn --version'
    }
	stage('maven validate ') {
	       
          sh 'mvn validate'
    }
	stage('sonar scan ') {
	       
          sh 'mvn sonar:sonar \
              -Dsonar.host.url=http://18.142.104.213:9000 \
              -Dsonar.login=a872146015635d0e3b67a3171a0435cfc5e16d31'
    }
	stage('maven compile') {
	       
          sh 'mvn compile'
    }
	stage('maven test') {
	       
          sh 'mvn test'
    }
	stage('maven package') {
	       
          sh 'mvn package'
    }
	stage('maven deploy') {
	       
          sh 'mvn deploy'
    }
}

