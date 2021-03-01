node ('master') {
stage('scm') {
    git 'https://github.com/vkcpride/game-of-life.git'
}
stage ('build') {
    sh 'mvn clean package'
}
stage('post build') {
    archive 'gameoflife-web/target/*.war'
    junit 'gameoflife-web/target/surefire-reports/*.xml'
}
}
