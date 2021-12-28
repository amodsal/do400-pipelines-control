node('nodejs') {
   parameters {
        booleanParam(name: "RUN_FRONTEND_TESTS", defaultValue: true)
   }
   
   stage('Checkout') {
      git branch: 'main',
      url: 'https://github.com/amodsal/do400-pipelines-control.git'
   }

   stage('backend Tests') {
      sh 'node ./backend/test.js'
   }

   stage('Frontend Tests') {
      sh 'node ./frontend/test.js'
   }
}
