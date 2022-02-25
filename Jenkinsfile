@Library('piper-lib-os') _
node() {
    stage('prepare'){
        checkout scm
        setupCommonPipelineEnviorment script: this
    }
    stage('build'){
        mtaBuild script: this
    }
    stage('deploy'){
        cloudFoundryDeploy script: this
    }
}