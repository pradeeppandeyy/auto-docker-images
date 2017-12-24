pipeline {
    agent any

    parameters {
        [choice(choices: 'ManualNewProject\nVALIDATIONCLUSTER_DUMMYPROJECT1\nINFRASANDBOXCLUSTER_DUMMYPROJECT1', description: '', name: 'projectOptions'),choice(choices: 'ocp-master.infra.paas.gcp-c.tst.kohls.com\n10.206.2.67.xip.io', description: '', name: 'CLUSTER_APP_DOMAIN'),credentials(credentialType: 'org.jenkinsci.plugins.plaincredentials.impl.StringCredentialsImpl', defaultValue: 'openshift-infrasandbox-sa-jenkins-text', description: '', name: 'openShiftToken', required: true),booleanParam(defaultValue: false, description: '', name: 'auto'),booleanParam(defaultValue: true, description: '', name: 'createnewproject'), booleanParam(defaultValue: true, description: '', name: 'editRolebindings'),booleanParam(defaultValue: true, description: '', name: 'editQuotas'),string(defaultValue: '', description: '', name: 'NAMESPACE'),string(defaultValue: '', description: '', name: 'PROJECT_DISPLAYNAME'),string(defaultValue: '', description: '', name: 'PROJECT_DESCRIPTION'),string(defaultValue: '', description: '', name: 'PROJECT_ADMIN_USER'),choice(choices: '4Gi\n8Gi\n16Gi\n32Gi\n64Gi\n128Gi\n256Gi\n512Gi\n1024Gi', description: '', name: 'HARD_MEMORY'), choice(choices: '2\n4\n6\n8\n10\n12\n16\n32\n64\n128', description: '', name: 'HARD_CPU')]
    }

    stages {
        stage("foo") {
            steps {
                echo "flag: ${params.ImageDistro}"
                echo "flag: ${params.PakageType}"
            }
        }
    }
}
