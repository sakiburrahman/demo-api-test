pipeline {
  agent any
  stages {
    stage('run collection') {
      steps {
        sh 'docker run -t postman/newman run -h'
        sh 'docker run -v ${WORKSPACE}:/etc/newman --workdir /etc/newman -t postman/newman run ./collection-file/api_test_postman_collection.json -e ./environment-file/api_test_postman_environment.json -r cli,htmlextra --reporter-htmlextra-export --color off --disable-unicode'
      }
    }
  }
}