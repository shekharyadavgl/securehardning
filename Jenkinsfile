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
                   def data = readFile(file: 'test.json')
                   println(data)
               }
           }
        }
    }
}
