pipeline {
agent any
   parameters {
        choice(
            choices: ['java' , 'nginx', 'mysql' , 'postgres' , 'tomcat'],
            description: '',
            name: 'package')
    }


   stages {
        stage ('select') {
            when {
                
                expression { params.package == 'java' }
            }
            steps {
                ansiblePlaybook become: true, inventory: '/etc/ansible/hosts', playbook: 'java.yml'

            }
        }
    }

}

