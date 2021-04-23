pipeline{
    agent any
    stages {

    stage('build'){
    steps{
    echo "Running ${env.BUILD_ID} on {env.JENKINS_URL}"
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

