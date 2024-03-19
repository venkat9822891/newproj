node {
    stage('Cont.Download') {
    git branch: 'qa', url: 'https://github.com/venkat9822891/newproj.git'
                            }
    stage('Cont.Build') {
    sh 'mvn  clean package'
                        }
    stage('Cont.Deploy') {
    deploy adapters: [tomcat9(credentialsId: '4a4de0a3-ccc1-4359-a1f0-b40e8681e062', path: '', url: 'http://172.31.0.27:8080')], contextPath: '/qaapp', war: '**/*.war'  
                         }
}
