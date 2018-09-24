node {
    checkout scm
    stage('Compile') {
        // Compile the app and its dependencies
        sh './gradlew assembleDebug'
      
    }
    stage('Build APK') {
        // Finish building and packaging the APK
        sh './gradlew assembleDebug'

        // Archive the APKs so that they can be downloaded from Jenkins
        archiveArtifacts '**/*.apk'
        }
}
