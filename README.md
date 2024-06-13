# Warning: Not ready for production (as on 14 June 2024)!

## slacker
slacker (you can also write it as "Slacker") is a framework written in Nim (as a [nimble](https://github.com/nim-lang/nimble) package) for creating [Slack](https://slack.com) app servers. Slacker takes inspiration from Slack's own framework [Bolt](https://api.slack.com/bolt) which is available in Python, JavaScript, and Java flavours.

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

Once you have created your project, add the following line to your project's `.nimble` file (there's only one such file in a project) in the root folder.

```nim
# your_project_name.nimble


requires "slacker >= 0.1.0"
```

### Usage
Here's how you can initialise your Slack app using `slacker`. Within 

```nim
# /src/your_project_name.nim

import slacker

app = slacker.New()

```

### License
MIT

PS: I can set apart only about one hour every day (cannot do anything on Sundays) to work on this for now. So, development on this would be extremely slow.

### To-do
- [ ] app initialising function/struct
- [ ] app.start method
- [ ] app.message method to listen to messages
- [ ] say proc to send a message
- [ ] app.action method to respond to named events
- [ ] app.message to take Regex as triggering message argument
- [ ] say proc to send message as "blocks"
...(to be completed)