pipeline {
    agent any 
    stages {
         stage('checkout') {
                steps {
                 git credentialsId: 'jenkins-user-github', url: 'https://github.com/stspro/devops-springboot'){
              // Get some code from a GitHub repository
              bat("""
              git config --global credential.username {GIT_USERNAME}
              git config --global credential.helper "!echo password={GIT_PASSWORD};
	 echo"
              git clone https://github.com/stspro/devops-springboot
              echo "pulled the code"
              """)
              echo "pulled the code"
              """)
	stage ('Initialize') {
            steps {
                bat( '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        stage('Build') { 
            steps {
		bat 'mvn -D clean install '
                
            }
        }
	//stage('Sonarqube') {
    environment {
        scannerHome = tool 'SonarQubeScanner'
    }
    steps {
        withSonarQubeEnv('sonarqube') {
            bat "${scannerHome}/bin/sonar-scanner"
        }
        timeout(time: 10, unit: 'MINUTES') {
            waitForQualityGate abortPipeline: true
        }
    }
}
        stage('Test') { 
            steps {
                // 
            }
        }
        stage('Deploy') { 
            steps {
                // 
            }
        }
    }
}
