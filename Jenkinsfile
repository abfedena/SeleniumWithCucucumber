pipeline {
    agent any
    tools { 
        maven 'M3'
        jdk 'jdk8' 
    }
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Build') {
            steps {
                bat 'mvn verify'
                
                echo 'This is a minimal pipeline.'
            }
        }
    }
}
