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
            steps {
                withAnt(installation: 'Ant 1.9.2') {
                    sh "ant dist"
                }
            }
        }
    }
}
