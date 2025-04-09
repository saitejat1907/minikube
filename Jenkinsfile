pipeline {
    agent any

    stages {
        stage("Create Service Accounts") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 playbook: 'playbook/service_accounts.yml'
            }
        }

        stage("Apply Role Bindings") {
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
