pipeline 
{
agent any
parameters 
{
booleanParam (defaultvalue: true, name: 'java', description: java)
booleanParam (defaultvalue: false, name: 'nginx', description: nginx)
booleanParam (defaultvalue: false, name: 'postgres', description: postgres)
booleanParam (defaultvalue: false, name: 'mysql', description: mysql)
booleanParam (defaultvalue: false, name: 'tomcat', description: tomcat)
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
