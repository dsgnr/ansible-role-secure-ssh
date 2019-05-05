pipeline {
    agent any
    stages {
        stage('Ansible Role Secure SSH') {
            agent {
                docker {
                    image 'dsgnr/ansible-molecule-docker'
                }
            }
            stages {
                stage('Molecule Lint') {
                    steps {
                        echo "Running Molecule Lint..."
                        sh 'molecule lint > molecule-lint.log'
                    }
                }
            }
            post {
                always {
                    recordIssues enabledForFailure: true
                }
                failure {
                    sh 'cat molecule-lint.log'
                }
            }
        }
    }
    post {
        always {
            deleteDir()
        }
    }
}
