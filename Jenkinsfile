pipeline{
    agent any
    stages {

    stage('build'){
    steps{
    echo "Running by  ${env.BUILD_ID}"
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
