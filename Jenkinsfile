pipeline {
    agent any
    stages {
        stage('build') {
            steps {
             script{         
     def filePath = readFile "${WORKSPACE}/test.json"                   

     def lines = filePath.readLines() 
                    for (line in lines) {                                            
                      build(job: "$line/branchName",
                        parameters:
                        [string(name: 'vertical', value: "${params.vert}"),
                        string(name: 'environment', value: "${params.env}"),
                        string(name: 'branch', value: "${params.branch}"),
                        string(name: 'project', value: "${params.project}")
                        ]
                    )
                        }  
                                       }
        }
    }
}
