
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/tJurassic174/specialtopics-ci-lab'
  }

  stage('Build') {
    // you should build this repo with a maven build step here
    try {
        withMaven (maven: 'maven3') {
            sh "mvn package"
        }
    } finally {
        junit 'build/reports/**/*.xml'
    }
  }
  // you should add a test report here
}
