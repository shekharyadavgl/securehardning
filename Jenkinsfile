pipeline {
    agent any
    stages {
        stage('build') {
            steps {
             script{
//             git branch: 'Your Branch name', credentialsId: 'Your crendiatails', url: ' Your BitBucket Repo URL '

// ##To read file from workspace which will contain the Jenkins Job Name ###
           
     def filePath = readFile "${WORKSPACE}/test.json"                   

// ##To read file line by line ###
 
     def lines = filePath.readLines() 
      
// ##To iterate and run Jenkins Jobs one by one ####

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
