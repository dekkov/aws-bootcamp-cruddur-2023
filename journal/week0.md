# Week 0 — Billing and Architecture

### Install AWS CLI


Install AWS CLI on Gitpod using the docs from 
```https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html```

Update .gitpod.yml file so that it automatically install aws everytime it opens
```
tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
```

### Set up gitpod env variables and loacl env variables using 

local env: 
```
export AWS_ACCESS_KEY_ID=""
export AWS_SECRET_ACCESS_KEY=""
export AWS_DEFAULT_REGION=us-west-2
```

gitpod env:
```
gp env AWS_ACCESS_KEY_ID=""
gp env AWS_SECRET_ACCESS_KEY=""
gp env AWS_DEFAULT_REGION=us-west-2
```


### Check if AWS CLI is working:

```
aws sts get-caller-identity
```



