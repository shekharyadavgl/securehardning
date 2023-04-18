pipeline {
    agent any
    stages {
        stage('build') {
            steps {
script {
                   def date = new Date()
                   def data = "Hello World\nSecond line\n" + date
                   writeFile(file: 'zorg.txt', text: data)
                   sh "ls -l"
               }
                  }
        }
    }
}
