pipeline {
    agent any

    stages {
    //     stage("Installing Kubernetes Module") {
    //         steps {
    //             ansiblePlaybook credentialsId: 'Ansible',
    //                              disableHostKeyChecking: true,
    //                              installation: 'Ansible',
    //                              inventory: 'dev.inv',
    //                              playbook: 'playbook/prereq.yml'
    //         }
    //     }

    //     stage("Create Service Accounts") {
    //         steps {
    //             ansiblePlaybook credentialsId: 'Ansible',
    //                              disableHostKeyChecking: true,
    //                              installation: 'Ansible',
    //                              inventory: 'dev.inv',
    //                              playbook: 'playbook/service_accounts.yml'
    //         }
    //     }

    //     stage("Apply Role Bindings") {
    //         steps {
    //             ansiblePlaybook credentialsId: 'Ansible',
    //                              disableHostKeyChecking: true,
    //                              installation: 'Ansible',
    //                              inventory: 'dev.inv',
    //                              extraVars: [limit: 'n1'],
    //                              playbook: 'playbook/complete-setup.yml'
    //         }
    //     }

    //     stage("Create Secret") {
    //         steps {
    //             ansiblePlaybook credentialsId: 'Ansible',
    //                              disableHostKeyChecking: true,
    //                              installation: 'Ansible',
    //                              inventory: 'dev.inv',
    //                              playbook: 'playbook/postgres-secret.yml'
    //         }
    //     }

        // stage("postgres deployment") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'playbook/postgres-deployment.yml'
        //     }
        // }

        // stage("postgres service") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'playbook/postgres-service.yml'
        //     }
        // }
        

        // stage("be_docker_image_build") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'docker/lms-be.yml'
        //     }
        // }

        // stage("config maps") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'playbook/config_maps.yml'
        //     }
        // }

        // stage("backend deployment and service") {
        //     steps {
        //         ansiblePlaybook credentialsId: 'Ansible',
        //                          disableHostKeyChecking: true,
        //                          installation: 'Ansible',
        //                          inventory: 'dev.inv',
        //                          playbook: 'playbook/be-deploy.yml'
        //     }
        // }
        stage("frontend configmaps") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 playbook: 'playbook/config_maps.yml'
            }
        }

        stage("frontend deployment and service") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 playbook: 'playbook/fe-deploy.yml'
            }
        }
    }
}
