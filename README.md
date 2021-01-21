### About

`orgleaks` is a tool to run `gitleaks` for an organization. After version 7 of gitleaks the `--org` parameter was no longer supported. This small shell script helps you perform scans on an organization as well as allows you to pass arguments to gitleaks. 

Please note: This is not a full git scanning / secret scanner, to use this script you require [gitleaks](https://github.com/zricethezav/gitleaks) to be installed.

### Installation

Make sure you have installed [gitleaks](https://github.com/zricethezav/gitleaks/releases), then:

```
git clone https://github.com/thecybermafia/orgleaks.git
```
Please make sure you have updated your access token or placed an environment variable for the same inside the script, I would recommend you not to hardcode your access token. 

If you are not aware about access tokens, refer to [this](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) documentation given by Github.

### Usage

```
                         .__                 __
     ___________  ____   |  |   ____ _____  |  | __  ______
    /  _ \_  __ \/ ___\  |  | _/ __ \__  \ |  |/ / /  ___/
   (  <_> )  | \/ /_/  > |  |_\  ___/ / __ \|    <  \___ \
    \____/|__|  \___  /  |____/\___  >____  /__|_ \/____  >
               /_____/             \/     \/     \/     \/


  orgleaks.sh ver. 0.1
  To run gitleaks for an organization

  Usage: orgleaks.sh [-h|--help] [-o|--org github] [-v] [-a|--gitleaks-args]

  Options:
  -h, --help  Display this help message and exit.
  -o, --org, github  Organization Name
      where 'github' is the Organization Name.
  -v  verbose
  -a, --gitleaks-args, "--report=org-gitleaks-result --format=csv"
      where '"--report=org-gitleaks-result --format=csv"' are the arguments for Gitleaks
      refer to https://github.com/zricethezav/gitleaks/wiki/Scanning

  Examples:

  orgleaks.sh -o github
  Scans the 'github' organization

  orgleaks.sh -o github -v
  Scans the 'github' organization and enables verbosity

  orgleaks.sh -o github -v -a "--report=github-gitleaks-result.csv --format=csv"
  Scans the 'github' organization, enables verbosity and save the report in csv format with provided name


```

### License

[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
