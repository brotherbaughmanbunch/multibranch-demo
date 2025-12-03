properties([parameters([string(name: 'goVersion', defaultValue: '1.5.0', description: 'Which version of Go language to use.')])])
node {
    stage('Checkout') {
        checkout scm
    }
    stage('Main') {
        docker.image("golang:${params.goVersion}").inside {
            echo "Main"
        }
    }
    stage('Post') {
        echo "Post"
    }
}
