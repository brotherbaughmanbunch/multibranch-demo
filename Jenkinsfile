properties([parameters([string(name: 'goVersion', defaultValue: '1.5.0', description: 'Which version of Go language to use.')])])
node {
    stage('Checkout') {
        checkout scm
    }
    stage('Main') {
        docker.image("golang:${params.goVersion}").inside {
            sh '''
                go version
                go build -v hello-world.go
            '''
        }
    }
    stage('Post') {
        sh '''
            ls -l
            ./hello-world
        '''
    }
}
