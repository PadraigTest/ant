def branch_name = env.BRANCH_NAME != null ? env.BRANCH_NAME : 'master'

pipeline {
    agent any


    stages {
        stage('test') {
            steps {
                echo "We have run the tests against ant job"
            }
        }
        stage('build and publish') {
            environment {
				IS_JENKINS = "true"
            }
            steps {
                    sh "ant helm-publish -verbose"
            }
        }
    }
}
