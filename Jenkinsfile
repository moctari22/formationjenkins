def mvn
node {
    stage('Get tools') {
        def maven_home = tool 'maven385'
        mvn = "${maven_home}/bin/mvn"
    }
    stage('Get maven version') { 
        bat "${mvn} --version"
    }       
}
