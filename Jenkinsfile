#!/usr/bin/groovy

// import com.anaplan.buildtools.jenkins_pipelines.ContainerTemplates
// import com.anaplan.buildtools.jenkins_pipelines.DefaultConfig

// @Library(['Anaplan_Pipeline', 'Security_Library'])

// this strange ID is the yeti repository ID - you can find these in https://anaplansite.atlassian.net/wiki/spaces/EP/pages/32309622/List+of+Git+repositories
def REPO_ID = "9363"

// Branch variables
def MAINLINE_BRANCH = "main"
def RELEASE_BRANCH_PREFIX = "release/"
def IS_MAINLINE = env.BRANCH_NAME == MAINLINE_BRANCH
def IS_RELEASE = env.BRANCH_NAME.startsWith(RELEASE_BRANCH_PREFIX)
def IS_MAINLINE_OR_RELEASE = IS_MAINLINE || IS_RELEASE

// Build variables
def VERSION

def BUILD_LABEL = "seceng-security-release-review-automation-build.${UUID.randomUUID().toString()}"
def ACCOUNT = "seceng"
def FEATURE = "seceng"
def SERVICE = "security-release-review-automation"

def GITHUB_ORG = "seceng"
def GITHUB_REPO = "security-release-review-automation"

// Notification Variables
def SLACK_CHANNEL = "#security-hardening-application-developer"

pipeline {
     agent any
//     agent {
//         kubernetes {
//             label "${BUILD_LABEL}"
//             yaml pod(
//                 ContainerTemplates.dockerBuildContainers() + [
//                     ContainerTemplates.maven([:], "3.6-jdk-11"),
//                     securityToolboxContainer()
//                 ]
//             )
//         }
//     }

//     options {
//         disableConcurrentBuilds()
//         buildDiscarder(logRotator(daysToKeepStr: "30"))
//         timeout(time: 10, unit: "MINUTES")
//     }
stages {

    stage("Code Scan") {
        steps {
        echo "${BUILD_LABEL}"
//             doCodeScan(
//                 repo: REPO_ID,                                 // OPTIONAL: The gitHub repo name, if not supplied, then it is derived from Git URL
//                 slackChannel: SLACK_CHANNEL,                   // OPTIONAL: The slack channel where the messages should be sent if violations are found
//                 buildResultOnPolicyViolation: 'FAILURE',       // OPTIONAL: Choose the build status when the scan results in security findings, UNSTABLE is used as default
//             )
        }
     }
}
}
