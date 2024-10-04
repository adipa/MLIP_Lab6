pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: Running pytest with Python virtual environment (mlip)'

                # Activate the virtual environment
                source mlip/bin/activate

                # Run pytest in the activated virtual environment
                pytest

                # Uncomment the line below after successfully running the pytest command
                # exit 1
                # comment or remove this line after implementing the Jenkinsfile
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
