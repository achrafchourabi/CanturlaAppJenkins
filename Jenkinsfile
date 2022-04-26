pipeline
{

agent any
 stages {
  
   stage('PULL') {

   steps {
   
   script {

checkout([$class: 'GitSCM', branches: [[name: '*/master']],

userRemoteConfigs: [[

credentialsId: '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',
url: 'https://github.com/achrafchourabi/CanturlaAppJenkins.git' ]]])



}
}
}


stage('build') {
steps{

script {

sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml "

}
}
}





}
}
