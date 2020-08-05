# aws-codebuild-extras ![Build Status](https://codebuild.us-west-2.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiUkxsV0l4UDBkWmh1Z1NIbm9wTENycVl4d1pDTTYrc1I3dzhFSlQ1QWFQdDl1Tm10NGduZklrTWVON1Vock5rOHVJV0xGYWhwT0V0cWVtMFg2WWRLTVlZPSIsIml2UGFyYW1ldGVyU3BlYyI6InhrOHdIV0FzY3Y1dmZ0SGwiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=master)
Adds extra information of your AWS CodeBuild build via environment variables.

## Usage

Add the following command to the `install` or `pre_build` phase of your buildspec:

    curl -fsSL https://raw.githubusercontent.com/thii/aws-codebuild-extras/master/install >> extras.sh && . ./extras.sh

You can also break the installation into two steps to improve readability.
For example in the `install` phase:
```
phases:
  install:
    commands:
      - echo Installing codebuild-extras...
      - curl -fsSL https://raw.githubusercontent.com/thii/aws-codebuild-extras/master/install >> extras.sh
      - . ./extras.sh
```
|NAME|VALUE
|---|---|
|CI|true|
|CODEBUILD|true|
|CODEBUILD_GIT_AUTHOR|Committer Name|
|CODEBUILD_GIT_AUTHOR_EMAIL|user@example.com|
|CODEBUILD_GIT_BRANCH|branch name|
|CODEBUILD_GIT_COMMIT|commit hash|
|CODEBUILD_GIT_MESSAGE|commit message|
|CODEBUILD_GIT_TAG|git tag|
|CODEBUILD_PROJECT|project|
|CODEBUILD_PULL_REQUEST|Pull request number|
