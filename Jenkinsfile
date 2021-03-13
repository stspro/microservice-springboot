pipeline {
    agent any 
    stages {
         stage('checkout') {
                steps {

              bat("""
              
              git clone https://github.com/stspro/devops-springboot
              echo "pulled the code"
              """)
	}
	}
	stage ('Initialize') {
            steps {
                bat( """
                   set PATH
                    set M2_HOME
					set 
                """)
				step{
	pwd
	bat "DIR"
	bat "set "
				}
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
