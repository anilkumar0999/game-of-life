node('UBUNTU'){
    stage('scm'){
        git 'https://github.com/anilkumar0999/game-of-life.git'

    }

    stage('build'){
        sh 'mvn package'

    }

    stage('postbuild'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
        
        archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false

    }

}
