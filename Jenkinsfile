pipeline{
    agent any
    stages {

    stage('build'){
    Steps{
    echo "Running ${env.BUILD_ID} on {env_JENKINS_URL}"
    sh 'ant -f build.xml -v'
    }
    }
    }
    post {
   	 always{
   		 archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
   	 }
    }
}

