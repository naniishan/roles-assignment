pipeline 
{
agent any
parameters 
{
booleanParam (defaultValue: true, name: 'java', description: java)
booleanParam (defaultValue: false, name: 'nginx', description: nginx)
booleanParam (defaultValue: false, name: 'postgres', description: postgres)
booleanParam (defaultValue: false, name: 'mysql', description: mysql)
booleanParam (defaultValue: false, name: 'tomcat', description: tomcat)
}

stages 
{
stage ('git') 
{
steps 
{
git 'https://github.com/naniishan/roles-assignment.git'
}
}
stage ('select')
{
when 

{
expression { ${params.java} == 'true' }
}
steps 
{
ansiblePlaybook inventory: '/etc/ansible/hosts', playbook: 'java.yml'
}
}

}
}
