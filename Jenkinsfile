pipeline {
  agent any
  stages {
    stage("cd /opt/tf") {
      /* step 1: clone the repo to workspace*/
      steps {
        sh "cd /opt/tf"
        echo "CDCDCDCDCD"
      }
    }
    stage("clone from git") {
      steps {
        sh "git pull"
        echo "PULLLLLLLLLLLLL"
      }
    }
    stage("pip install") {
      steps {
        sh "python3 -m pip instll -r  /opt/tf/requirements.txt"
        echo "PIPIPIPIPIPIPIPIP"
      }
    }
    stage("run app.py") {
      steps {
        sh "python3 /opt/tf/app.py"
        echo "RUNRUNRUN"
      }
    }
  }
}
