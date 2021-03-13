pipeline {
    agent any 
    stages {
         stage('checkout') {
                steps {
                
	 bat (echo"
              git clone https://github.com/stspro/devops-springboot
              echo "pulled the code"
              """)
              echo "pulled the code"
              """)
	}
	}
	stage ('Initialize') {
            steps {
                bat( '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''')
            }
	
	}
        stage('Build') { 
            steps {
		bat 'mvn -D clean install '
                
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
