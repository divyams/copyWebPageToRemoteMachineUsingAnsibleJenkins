pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git 'https://github.com/divyams/copyWebPageToRemoteMachineUsingAnsibleJenkins.git'
            }
        }

        stage('build') {
            steps {
                ansiblePlaybook(
                    credentialsId: '9d08a7bd-049c-4522-a46f-222c98101801',
                    disableHostKeyChecking: true,
                    installation: 'ansible',
                    inventory: 'dev.inv',
                    playbook: 'copy.yml'
                )
            }
        }
    }
}