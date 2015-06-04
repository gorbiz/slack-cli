slack-cli
=========
A very simple command line interface (CLI) for [Slack](https://slack.com).

Send a message
--------------

    slackcli -t slack_token -g group_name -m "Hello World!"
    
Or if the environment variable [`SLACK_TOKEN`](https://api.slack.com/web) is set, you can simply use,

    slackcli -g group_name -m "Hello World!"

Send a file
-----------

    slackcli -t slack_token -g group_name -f filename -m "Download this file"

Send from standard input
------------------------

    # slackcli -t slack_token -g group_name -c
    Hello World!
    #

Install
-------
With npm do:

    npm install -g slack-cli

Usage
-----

    # slackcli --help
    USAGE: node <SOMEWHERE>\npm\node_modules\slack-cli\bin\cmd.js [OPTION1] [OPTION2]... arg1 arg2...
    The following options are supported:
      -m, --message <ARG1>  Specify the text of the message to send
      -g, --group <ARG1>    Specify the group name (mandatory)
      -f, --file <ARG1>     Specify the name of the file to send
      -t, --token <ARG1>    Specify the Slack API token
      -v, --verbose         Set to verbose mode
      -c, --console         Use console to input message
      -w, --waitText <ARG1>         Specify the text message to wait.  Default timeout is 30 seconds.
      -s, --timeout <ARG1>          Specify the seconds to timeout when using --waitText.

Advanced Mode
-------------
To reuse the [Slack token](https://api.slack.com/web), you can set the token as the environment variable `SLACK_TOKEN` like this.

    set SLACK_TOKEN=xoxo-12345678-12345678-12345678-123abc

