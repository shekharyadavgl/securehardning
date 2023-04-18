pipeline {
    agent any
    stages {
        stage('build') {
            steps {
script {
                   def date = new Date()
                   def data = "Hello World\nSecond line\n" + date
                   def data2 = readFile(file: 'test.json')
                   println(data2)
                   sh "ls -l"
               }
                  }
        }
    }
}
