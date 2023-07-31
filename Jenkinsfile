pipeline {
    agent any 

    stages {
        stage ('Build') {
            parallel{
                stage("API Pipeline") {
                    steps {
                        build(job: 'api-pipeline', scriptPath: 'api-jenkinsfile.groovy')
                    }
                }
                
                stage("Web pipeline") {
                    steps {
                        build(job: 'web-pipeline', scriptPath: 'web-jenkinsfile.groovy')
                    }
                }
            }
        }
    }
}
