node() {
// the workspace in jenkins Master
//
stage('Retrieve source code') {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'cf1bc2fe-f915-446f-9501-f225ef8fbc50', url: 'https://github.com/kubernates/ansible.git']]])
    }
stage('Ansible playbook') {
      
        ansiblePlaybook installation: 'default', inventory: '/var/lib/jenkins/workspace/ansibletest/hosts', playbook: '/var/lib/jenkins/workspace/ansibletest/ping.yml'
        //sh "mvn clean package -Dbuild.number=${BUILD_NUMBER}"
        //sh "/bin/mv -f $WORKSPACE/target/*.war $WORKSPACE/Build-${env.BUILD_NUMBER}/vsvyadav_${env.BRANCH_NAME}${env.BUILD_NUMBER}.war"
        //sh "/bin/cp -f $WORKSPACE/Build-${env.BUILD_NUMBER}/vsvyadav_${env.BRANCH_NAME}${env.BUILD_NUMBER}.war $WORKSPACE/vsvyadav.war"
      
    }
}
 
