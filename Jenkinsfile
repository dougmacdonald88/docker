node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("doug/web")
    }

    stage('Run image') {
        /* Spin up image */

       docker.image('doug/web').withRun(' -p 80:80')
    }

}