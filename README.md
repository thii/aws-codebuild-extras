# aws-codebuild-extras ![Build Status](https://codebuild.us-west-2.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiUkxsV0l4UDBkWmh1Z1NIbm9wTENycVl4d1pDTTYrc1I3dzhFSlQ1QWFQdDl1Tm10NGduZklrTWVON1Vock5rOHVJV0xGYWhwT0V0cWVtMFg2WWRLTVlZPSIsIml2UGFyYW1ldGVyU3BlYyI6InhrOHdIV0FzY3Y1dmZ0SGwiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=master)
Add extra information of your AWS CodeBuild build via environment variables.

## Usage

Add the following command to the `install` or `pre_build` phase of your buildspec:

    bash -c "$(curl -fsSL https://raw.githubusercontent.com/thii/aws-codebuild-extras/master/install)"
