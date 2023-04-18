pipeline {
    agent any
    stages {
        stage('build') {
            steps {
script {
                   def date = new Date()
                   def data = "Hello World\nSecond line\n" + date
                   writeFile(file: 'zorg.txt', text: data)
                   def data = readFile(file: 'zorg.txt')
                   println(data)
                   def data = readFile(file: 'test.json')
                   println(data)
                   sh "ls -l"
               }
                  }
        }
    }
}
