pipeline {
agent any
Open with Google Docs
stages {
stage('Build') {
steps {
build 'PES1UG22CS813-1'
sh 'g++ main.cpp -o output'
}
}
stage('Test') {
steps {
sh './output'
}
}
stage('Deploy') {
steps {
echo 'deploy'
}
}
}
post{
failure{
error 'Pipeline failed'
}
}
}
