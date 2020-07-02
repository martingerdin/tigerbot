![](tiger-emoji.png)

# tigerbot

[![Automated Release Notes by gren](https://img.shields.io/badge/%F0%9F%A4%96-release%20notes-00B2EE.svg)](https://github-tools.github.io/github-release-notes/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**`tigerbot` is really a cub more than a fully grown tiger**

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
cd tigerbot
chmod +x tigerbot
```

Or:

```
mkdir tigerbot
cd tigerbot
wget https://github.com/martingerdin/tigerbot/master/tigerbot
chmod +x tigerbot
```

## Usage

Note that to use `tigerbot` you need a Slack API token. `tigerbot`
assumes that this token is stored in a `.env` file in the current
working directory.

```
# Get help
./tigerbot

# Install required R packages
./tigerbot install

# Send IM to member
./tigerbot username "Hello, I'm tigerbot!"

# Send message to channel
./tigerbot general "Hello, I'm tigerbot" --channel

# Send message directly, without being prompted to confirm
./tigerbot general "Hello, I'm tigerbot" --channel --no-confirm
```

