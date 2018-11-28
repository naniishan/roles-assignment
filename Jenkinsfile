pipeline {
agent any

properties([parameters([choice(choices: ['nginx,java,tomcat,mysql,postgres'], description: '', name: 'select')])])



#stage ('select'){
stages {



stage ('print'){
steps {
    when {
          
                expression { params.select == 'java' }
            }

steps {

ansiblePlaybook become: true, inventory: '/etc/ansible/hosts', playbook: 'java.yml'


}
}
}


s

}




}
