def repo="https://github.com/hpkaur86/helm4liveRamp"
pipeline{
         agent any
	 stages {
                stage('build') {
                   steps {
                     sh "helm package helm4liveramp; helm registry login -u liveramp-cicd-e516f62f9b7c.json --password-stdin https://us-central1-docker.pkg.dev; gcloud auth configure-docker us-central1-docker.pkg.dev ;  helm push helm4liveramp-0.0.1.tgz oci://us-central1-docker.pkg.dev/liveramp-cicd/quickstart-helm-repo"
                }
                }
                stage('deploy') {
                   steps {
                     sh " "
                }
               }
        }
}
