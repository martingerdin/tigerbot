![](tiger-emoji-small.png)

# tigerbot (v1.0.3)

[![Automated Release Notes by gren](https://img.shields.io/badge/%F0%9F%A4%96-release%20notes-00B2EE.svg)](https://github-tools.github.io/github-release-notes/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

`tigerbot` is a small utility and slack app that allows the user to
communicate with `teambengaltiger` over the command line. We use it to
send automated messages from our servers. Future use cases might
include to distribute data review reports, get data summaries, submit
non-sensitive data etc.

## Dependencies
`tigerbot` is written in `R`, so you need a working installation of
`R` for `tigerbot` to work. The specific `R` packages needed can be
installed using `tigerbot` itself.

## Installation

```
git clone https://github.com/martingerdin/tigerbot.git
sudo mv tigerbot /opt/
sudo chmod +x /opt/tigerbot/tigerbot
sudo ln -s /opt/tigerbot/tigerbot /usr/local/bin/ # symlink into /urs/local/bin
```

Or:

```
sudo mkdir /opt/tigerbot
sudo wget https://raw.githubusercontent.com/martingerdin/tigerbot/master/tigerbot -P /opt/tigerbot/
sudo chmod +x /opt/tigerbot/tigerbot
sudo ln -s /opt/tigerbot/tigerbot /usr/local/bin/ # symlink into /urs/local/bin
```

## Usage

Note that to use `tigerbot` you need a Slack API token. `tigerbot`
assumes that this token is stored in a `.env` file in the current
working directory or in the default installation directory
`/opt/tigerbot/`.

```
# Get help
tigerbot --help

# Install required R packages
tigerbot install

# Send IM to member using its full name 
tigerbot Gary "Hello, I'm tigerbot!"

# Send IM to member using its email
tigerbot gary@example.com "Hello, I'm tigerbot!" --email

# Send message to channel
tigerbot general "Hello, I'm tigerbot" --channel

# Send message directly, without being prompted to confirm
tigerbot general "Hello, I'm tigerbot" --channel --no-confirm

# Send file to channel
tigerbot general foo.txt --channel --file

# Send file with title and initial comment
tigerbot general foo.txt --channel --file --file-title Bar \
  --initial-comment "A file with title and comment"
```

