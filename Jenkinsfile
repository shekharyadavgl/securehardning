pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "Hello World!"
            }
       stage('read') {
           steps {
               script {
                   def data = readFile(file: 'zorg.txt')
                   println(data)
               }
           }
        }
    }
}
