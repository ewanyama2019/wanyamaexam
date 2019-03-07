node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t wanyamaexam:latest ."
}

stage('Docker login to hub and Apply docker tag'){
sh "docker login -u 'ewanyamadockerxt' -p '1Mdcccl3x3' "
sh "docker tag wanyamaexam:latest ewanyamadockerxt/wanyamaexam:latest"
}

stage('push the image') {
sh "docker push ewanyamadockerxt/wanyamaexam:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
