pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "Hello World!"
                env.WORKSPACE = pwd()
                def filejson = readFile "${env.WORKSPACE}/test.json"
                echo filejson
            }
        }
    }
}
