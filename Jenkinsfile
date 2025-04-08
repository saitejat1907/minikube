pipeline {
    agent any

    stages {
        stage("Execute Ansible") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 playbook: 'playbook/service_accounts.yml'
            }
        }

        stages {
        stage("Execute Ansible") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 extraVars: ['limit=n1'],
                                 playbook: 'rolebinding/complete-setup.yml'
            }
        }
    }
}