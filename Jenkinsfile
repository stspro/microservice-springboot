pipeline {
    agent any 
    stages {
         stage('checkout') {
                steps {
                 //git  url: 'https://github.com/stspro/devops-springboot'
              // Get some code from a GitHub repository
              bat("""
              
	 echo"
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
                   set PATH
                    set M2_HOME
	set echo "M2_HOME = ${M2_HOME}"
                ''')
	pwd
	bat "DIR"
	bat "set "
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
