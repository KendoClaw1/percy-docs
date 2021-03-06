# Setup: Jenkins

[!INCLUDE /docs/setup/-preamble]

## Jenkins build setup

Depending on how you have Jenkins configured, there are a few options for configuring environment variables.

You can use the [EnvInject plugin](https://wiki.jenkins-ci.org/display/JENKINS/EnvInject+Plugin) to set these environment variables for a build:

[!INCLUDE /docs/setup/-env-vars-setup-list]

Alternatively you could export the variables as part of the build script:

```bash
export PERCY_TOKEN=aaabbbcccdddeeefff
export PERCY_PROJECT=my-org/repo-name

# Now run your tests (just an example, this depends on the client library used):
bundle exec rspec
```

<div class="Alert Alert--warning">

**IMPORTANT: Keep your Percy token secret.** Anyone with access to your token can consume your account quota, though they cannot read data.

If your code is public, do not commit the PERCY_TOKEN to your code.

</div>

[!INCLUDE /docs/setup/-next-step-clients]
[!INCLUDE /docs/-client-list]
