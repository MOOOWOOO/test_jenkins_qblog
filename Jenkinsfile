pipeline {
  environment {
      // 部署远程主机ip地址,需要通过密钥的方式设置免密登录
      remoteIp = "192.168.0.234"
      remoteName = "root"
      remotePort='22'
  }
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
