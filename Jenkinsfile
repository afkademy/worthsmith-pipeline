pipeline {
    agent any 

    stages {
        parallel {
            stage ("API") {
                steps {
                    build(job: 'api-pipeline', file: 'api-jenkinsfile.groovy')
                }
            }

            stage("Web") {
                steps {
                    build(job: 'web-pipeline', file: 'web-jenkinsfile.groovy')
                }
            }
        }
    }

}