node{

stage('Clone Repository')

{
checkout scm
}
stage('Show me the files')
{
sh "ls -1"
}

stage('Build docker image')
{
sh "docker build -t docker_test:latest ."
}
stage('Docker login to hub and push  the image')
{
sh "docker login -u 'naisenyamungai' -p 'Delta9927046' "
sh "docker tag dockerfile_naisenya:version1 naisenyamungai/dockerfile_naisenya:version1"
sh "docker push naisenyamungai/dockerfile_naisenya:version1"
}
stage('Apply changes to the environment'){
sh "ls -1"
}

}
