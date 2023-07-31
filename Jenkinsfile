pipeline {
    agent any 

    stages {
        stage ('Build') {
            parallel{
                stage("API Pipeline") {
                    steps {
                        build(job: 'api-pipeline', file: 'api-jenkinsfile.groovy')
                    }
                }
                
                stage("Web pipeline") {
                    steps {
                        build(job: 'web-pipeline', file: 'web-jenkinsfile.groovy')
                    }
                }
            }
        }
    }
}