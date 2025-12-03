properties([parameters([string(name: 'goVersion', defaultValue: '1.5.0', description: 'Which version of Go language to use.')])])
node {
    stage('Checkout') {
        checkout scm
    }
    stage('Main') {
        echo "Main"
    }
    stage('Deploy to Prod') {
        input message: 'Ready to deploy to Prod?', ok: 'Yes', cancel: 'No'
        echo 'Deploying...'
    }
    stage('Post') {
        echo "Post"
    }
}
