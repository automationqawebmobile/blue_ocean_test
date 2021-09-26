pipeline {
  agent {
    node {
      label 'linux'
    }

  }
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/automationqawebmobile/test.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install -Dsurefire.suiteXmlFiles=Testng.xml  -Dlog4j.configurationFile=src//main//resources//log4J2.xml  -B'
      }
    }

  }
}