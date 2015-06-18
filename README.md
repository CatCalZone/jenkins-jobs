# CatCalZone Jenkins Job Definitions

These are the Jenkins job definitions for CatCalZone [Jenkins Job DSL Plugin](https://wiki.jenkins-ci.org/display/JENKINS/Job+DSL+Plugin).

Changes on the `master` branch of this repository will be [applied by a seed job](https://github.com/jenkinsci/job-dsl-plugin/wiki/Tutorial---Using-the-Jenkins-Job-DSL#1-creating-the-seed-job)
every 5 minutes.

## Usage

Since everything you push to `master` will be applied to our production Jenkins you typically want to test your changes on a feature branch / in an isolated environment first.

1. create a feature branch, e.g. `git checkout -b feature/add-xyz-job`
1. spin up a local VM with [our Jenkins server](https://github.com/Zuehlke/cookbooks-jenkins-simple-app): `vagrant up`
1. go to http://localhost:8080
1. add a new freestyle job [with a "Process Job DSL" builder](https://github.com/jenkinsci/job-dsl-plugin/wiki/Tutorial---Using-the-Jenkins-Job-DSL)
1. test your job definition there (see [Job DSL Commands](https://github.com/jenkinsci/job-dsl-plugin/wiki/Job-DSL-Commands))
1. push your feature branch, e.g. `git push -u origin feature/add-xyz-job`
1. create a [pull request](https://github.com/CatCalZone/jenkins-jobs/pulls) for easier peer review with your mates
1. merge the pull request
