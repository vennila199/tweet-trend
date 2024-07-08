pipeline {
    agent {
        node {
            label 'maven-slave2'
        }
    }
environment {
    PATH = "/opt/apache-maven-3.9.8/bin:$PATH"
}
    stages {
        stage("build"){
            steps {
                 echo "----------- build started ----------"
                sh 'mvn clean deploy -Dmaven.test.skip=true'
                 echo "----------- build complted ----------"
            }
        }
    }

}