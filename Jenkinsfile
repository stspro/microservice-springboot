node {
	

         stage('checkout') {
		 environment {
       env.PATH = env.PATH + ";c:\\Windows\\System32"
   }

		 pwd()
		 
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
		bat 'cd demo'
		bat "DIR"
		//bat 'mvn -D clean install '
		bat( """
		   	cd demo
		    	mvn -D clean install 
		""")
		archiveArtifacts artifacts: 'demo\target/*.jar'
		bat "DIR"
	//	dir('demo')
	//	{
	//		bat 'mvn -D clean install '
	//	}
                

        }

        stage('Test') { 

        }
        stage('Deploy') { 

        }

}
