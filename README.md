# lambda-demo
## version

## how to develop
### create enviroment
$ brew install docker
$ brew tap aws/tap
$ brew install aws-sam-cli
$ sam init

logs
hoge create-lambdademo % brew install docker
Running `brew update --preinstall`...
==> Auto-updated Homebrew!
Updated 2 taps (homebrew/core and aws/tap).
==> New Formulae
fb303                  kopia                  numdiff                tagref                 tarlz                  webp-pixbuf-loader     websocketpp            xidel
==> Updated Formulae
Updated 142 formulae.

==> Downloading https://ghcr.io/v2/homebrew/core/docker/manifests/20.10.12
######################################################################## 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/docker/blobs/sha256:e0f0f587866b5e53f620f9c7d478fd0679c4bfb10522b1bc2697c61868c2c6f4
==> Downloading from https://pkg-containers.githubusercontent.com/ghcr1/blobs/sha256:e0f0f587866b5e53f620f9c7d478fd0679c4bfb10522b1bc2697c61868c2c6f4?se=2022-02-12T01%3A40%3A00Z&sig=A
######################################################################## 100.0%
==> Pouring docker--20.10.12.arm64_monterey.bottle.tar.gz
==> Caveats
zsh completions have been installed to:
  /opt/homebrew/share/zsh/site-functions
==> Summary
🍺  /opt/homebrew/Cellar/docker/20.10.12: 12 files, 58.5MB
==> Running `brew cleanup docker`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
hoge create-lambdademo % brew tap aws/tap
hoge create-lambdademo % brew install aws-sam-cli

Warning: aws/tap/aws-sam-cli 1.37.0 is already installed and up-to-date.
To reinstall 1.37.0, run:
  brew reinstall aws-sam-cli
hoge create-lambdademo % sam init
Which template source would you like to use?
        1 - AWS Quick Start Templates
        2 - Custom Template Location
Choice: 1

Cloning from https://github.com/aws/aws-sam-cli-app-templates

Choose an AWS Quick Start application template
        1 - Hello World Example
        2 - Multi-step workflow
        3 - Serverless API
        4 - Scheduled task
        5 - Standalone function
        6 - Data processing
        7 - Infrastructure event management
        8 - Machine Learning
Template: 1

 Use the most popular runtime and package type? (Nodejs and zip) [y/N]: N

Which runtime would you like to use?
        1 - dotnet5.0
        2 - dotnetcore3.1
        3 - go1.x
        4 - java11
        5 - java8.al2
        6 - java8
        7 - nodejs14.x
        8 - nodejs12.x
        9 - python3.9
        10 - python3.8
        11 - python3.7
        12 - python3.6
        13 - ruby2.7
Runtime: 10

What package type would you like to use?
        1 - Zip
        2 - Image
Package type: 1

Based on your selections, the only dependency manager available is pip.
We will proceed copying the template using pip.

Project name [sam-app]: hanson-lambda

    -----------------------
    Generating application:
    -----------------------
    Name: hanson-lambda
    Runtime: python3.8
    Architectures: x86_64
    Dependency Manager: pip
    Application Template: hello-world
    Output Directory: .
    
    Next steps can be found in the README file at ./hanson-lambda/README.md
        

    Commands you can use next
    =========================
    [*] Create pipeline: cd hanson-lambda && sam pipeline init --bootstrap
    [*] Test Function in the Cloud: sam sync --stack-name {stack-name} --watch

$ sam build

logs
sam build
Building codeuri: /Users/aokiyusuke/Downloads/inDire/samurai-task/create-lambdademo/hanson-lambda/hello_world runtime: python3.8 metadata: {} architecture: x86_64 functions: ['HelloWorldFunction']

Build Failed
Error: PythonPipBuilder:Validation - Binary validation failed for python, searched for python in following locations  : ['/usr/bin/python'] which did not satisfy constraints for runtime: python3.8. Do you have python for runtime: python3.8 on your PATH?
aokiyuuhajime@aokiyuuimenoMBP hanson-lambda % cd ..
aokiyuuhajime@aokiyuuimenoMBP create-lambdademo % sam build
Error: Template file not found at /Users/aokiyusuke/Downloads/inDire/samurai-task/create-lambdademo/template.yml
aokiyuuhajime@aokiyuuimenoMBP create-lambdademo % cd hanson-lambda 
aokiyuuhajime@aokiyuuimenoMBP hanson-lambda % sam build       
Building codeuri: /Users/aokiyusuke/Downloads/inDire/samurai-task/create-lambdademo/hanson-lambda/hello_world runtime: python3.8 metadata: {} architecture: x86_64 functions: ['HelloWorldFunction']

