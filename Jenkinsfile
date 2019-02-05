#!/usr/bin/env groovy

// Example Jenkinsfile using the pipeline shared library

@Library('jenkins_shared_library@officialArtifactVersioning') _

basicCredentialsExamplePipeline(
        appName: 'person',
        dockerImageName: 'person',
        appComponentName: 'person-service',
        gradleBuildTargets: 'person-service:clean person-service:build person-business:build test',
        gradleNexusTarget: 'person-service:publish',
        junitResults: 'person-business/build/test-results/**/*.xml',
        jacocoReportDir: 'person-business/build/reports/jacoco/test/html',
        slackChannel: '#cr_releases',
        codeCoveragePct: '0.5',
        codeCoverageDefFile: 'person-business/build.gradle'
        )
