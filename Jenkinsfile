pipeline {
  agent any
  stages {
    stage("cd /opt/tf") {
      /* step 1: clone the repo to workspace*/
      steps {
        sh "cd /opt/tf"
      }
    }
    stage("clone from git") {
      /* step 1: clone the repo to workspace*/
      steps {
        sh "git pull"
      }
    }
    // stage("build img") {
    //   steps {
    //     sh "docker build -t myflask:v1 ."
    //   }
    // }
    // stage("run img") {
    //   steps {
    //     sh "docker run -d --name myflask myflask:v1"
    //   }
    // }
    // stage("test") {
    //   steps {
    //     echo "testing"
    //   }
    // }
    stage("run app.py") {
      steps {
        sh "python3 /opt/tf/app.py"
      }
    }
  }
}
