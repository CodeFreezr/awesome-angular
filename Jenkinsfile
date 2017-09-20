pipeline {
  agent any
  stages {
    stage('MyStageOne') {
      steps {
        parallel(
          "MyStageOne": {
            sleep 1
            
          },
          "Step1": {
            echo 'Hello World in Stage1, Step1'
            
          }
        )
      }
    }
    stage('MyStageTwo') {
      steps {
        parallel(
          "MyStageTwo": {
            sleep 1
            
          },
          "Step 2.1": {
            isUnix()
            
          },
          "Step 2.2": {
            echo 'Hello Step 2.2'
            
          }
        )
      }
    }
    stage('FinalStage') {
      steps {
        pwd(tmp: true)
        echo 'Hi, Final Stage here'
      }
    }
  }
}