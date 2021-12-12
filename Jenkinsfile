pipeline {
  agent any
  stages {
    stage('Check Terraform against CIS') {
      steps {
        sh '''#!/bin/bash
cd simple-cluster
#terraform init
#terraform plan --out=plan_file
../../../bin/shiftleft.cli iac-assessment -i terraform -r -68 -p /var/lib/jenkins/workspace/terraform-azure_master/simple-cluster
'''
      }
    }

  }
}