@Library("mylibs") _
pipeline {
  agent any
/*  tools {
    maven 'maven2'
  } **/
  
  stages{
    when {
                branch 'master'
            }
    stage("Maven Build"){
      steps{
        echo "hey ankith"
      }
    }
    stage("Deploy To Dev"){
      steps{
        echo "hello world"
      }
    }
  }
}

