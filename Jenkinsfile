node {
    stage('Cont.Download') {
    git branch: 'test', url: 'https://github.com/venkat9822891/newproj.git'
                            }
    stage('Cont.Build') {
    sh 'mvn  clean package'
                        }
    stage('Cont.Deploy') {
    deploy adapters: [tomcat9(credentialsId: '1fa67e8f-996c-456b-94b4-3512d5a6c377', path: '', url: 'http://172.31.8.198:8080')], contextPath: '/testapp', war: '**/*.war'  
                         }
}
