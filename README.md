# Warning: Not ready for any use let alone production (as on 14 June 2024)!

## slacker
Slacker (you may also write it as "slacker") is a framework written in Nim (as a [nimble](https://github.com/nim-lang/nimble) package) for creating [Slack](https://slack.com) app servers. Slacker takes inspiration from Slack's own framework [Bolt](https://api.slack.com/bolt) which is available in Python, JavaScript, and Java flavours.

### Supported Nim version
\>= 2.0.4

### Installation
Make sure you have a working Nim installation; being a version equal to or greater than the one mentioned above. If you don't have Nim installed in your machine, you can install Nim by following the instructions [here](https://nim-lang.org/install.html).

Once you have Nim installed in your machine, you can install slacker using `nimble install`.

```bash
$ nimble install github.com/bsljth/slacker
```
Once you have installed slacker (the above scripts installs slacker for your system), you need to add it to your project. First, create your project using `nimble`

```bash
$ nimble init your_project_name
# answer all the prompted questions that follow
# ...

$ cd your_project_name
```

You can also create a project folder using `mkdir` and `cd` into it and run `nimble init`.

Once you have created your project, add the line: `requires "slacker >= 0.1.0"` to your project's `.nimble` file in the root folder (there's only one such file in a project).

```nim
# your_project_name.nimble

# Package

version       = "0.1.0"
author        = "[YOUR NAME]"
description   = "[DESCRIPTION]"
license       = "[LICENSE]"
srcDir        = "[SOURCE FOLDER]"
bin           = @["file_name"]


# Dependencies

requires "nim >= 2.0.4"
requires "slacker >= 0.1.0"
```

### Usage
Here's how you can initialise your Slack app using `slacker`. Within the `/src/` folder, add the following to your main (starting point) `.nim` file. Note: You can configure which should be your source directory for the project and which should be your starting point by configuring the `srcDir` and `bin` values in your `.nimble` file.

Add the following to your main `.nim` file.

```nim
# /src/your_project_name.nim

import slacker

let config = ?

app = slacker.New(config)
# config will contain the token and signing-secret.

let port = 3000

app.start(port)

```

### License
MIT

PS: I can set apart only about an hour every day (won't be working on Sundays) to work on this for now. So, development on this would be extremely slow.

### To-do
- [ ] app initialising function/struct
- [ ] app.start method
- [ ] app.message method to listen to messages
- [ ] say proc to send a message
- [ ] app.action method to respond to named events
- [ ] app.message to take Regex as triggering message argument
- [ ] say proc to send message as "blocks"

...(to be completed)