node {
	

         stage('checkout') {
		 environment {
       env.PATH = env.PATH + ";c:\\Windows\\System32"
   }

		 dir
		 
              bat("""
              
              git clone https://github.com/stspro/devops-springboot
              echo "pulled the code"
              """)

	}
	stage ('Initialize') {

		bat( """
		   set PATH
			set M2_HOME
			set 
		""")

		bat "DIR"
		bat "set "
	}
        stage('Build') { 

		bat 'mvn -D clean install '
                

        }

        stage('Test') { 

        }
        stage('Deploy') { 

        }

}
