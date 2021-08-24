node{
   stage('SCM Checkout'){
     git credentialsId: 'dd4b1fe0-d5ea-49fa-a34d-02f71b7d8fdc', url: 'https://github.com/manoj1998-cloud/new-tomcat.git'
   }
   stage('mavenbuild'){
      def mvnHome =  tool name: 'maven-3', type: 'maven'
      echo "this is maven bulid area"
   }
   stage('Deploy to Tomcat'){
       deploy adapters: [tomcat9(credentialsId: 'deployer', path: '', url: 'http://15.207.19.75:8080/')], contextPath: null, war: '**/*.war'
   }
}
