pipeline {
    agent any 
    stages {
        stage('Static Analysis') {
            steps {
                echo 'Run the static analysis to the code' 
            }
        }
        stage('Compile') {
            steps {
                echo 'Compile the source code' 
            }
        }
        stage('Security Check') {
            steps {
                echo 'Run the security check against the application' 
            }
        }
        stage('Run Unit Tests') {
            steps {
                echo 'Run unit tests from the source code' 
            }
        }
        stage('Run Integration Tests') {
            steps {
                echo 'Run only crucial integration tests from the source code' 
            }
        }
        stage('Publish Artifacts') {
            steps {
                echo 'Save the assemblies generated from the compilation' 
            }
        }

       stage ('Pull Ansible Playbook') {
           steps {
               ansiblePlaybook(credentialsId: 'private_key', inventory: 'inventory/aws_ec2.yml', playbook: 'ansibleec2               basics.yml')
           }
         }    		
	stage('Build Complete') {
            steps {
                echo 'Hello Technologists!'
            }
        }
    }
}
