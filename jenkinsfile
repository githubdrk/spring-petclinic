node {
    stage('scm'){
        git 'https://github.com/dummyrepos/spring-petclinic.git'
    }

    stage('maven'){
        sh 'mvn package'
    }
    
    stage('Sonar') {
        withSonarQubeEnv('SONAR-6.7.4') {
             sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'
        }
    }
}
