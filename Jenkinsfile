pipeline {
  agent any
  stages {
    stage('Get config details') {
      steps {
        echo 'testing'
      }
    }
    stage('executing shell') {
      steps {
        sh '''curl -XPOST "http://stldmonitor05.rgare.net/nagiosxi/api/v1/config/service?apikey=pZ4IUu7eSTGlP4SACfCCo7OesLUAFTVk9g2jN8RVhtg6Q8WonuhOU5inPddKm94O&pretty=1" -d "host_name=testapihost&service_description=test-{i}&check_command=check_ncpa_no_param!{i}&check_interval=5&retry_interval=5&max_check_attempts=2&check_period=24x7&contacts=nagiosadmin&notification_interval=5&notification_period=24x7&applyconfig=0"
'''
      }
    }
  }
}