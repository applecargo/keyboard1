# keyboard1

## a fork of 'button1' to construct a web-shared keyboard, playable together with network actors.

- paperjs-based keyboard layout drawing
- paperjs doesn't support multiple touching natively. we could use 'hammer.js' to do that. but this is TBD.
- but puredata synth is 4 voices ready. so if many peoples play together up to 4 peoples, it works fine.

## a copy of READMD.md of 'button1'

### concept

- a node express web server which serves a public webpage with single button UI
- this simple webpage will be accesible for smartphones and computers
- button touch/click will generate websocket messages which will travel to one computer that is running puredata and/or supercollider for sound performances

### notes

- this server supports https protocol and automatic redirection of http to https
- to make connections go global and unlimited by any physical spaces, run app.js @ e.g. amazon aws ec2 server, and then connect to it as a client: run receiver.js @ localhost
- for smartphones, LTE connection is recommended. 'cause one wifi router can handle limited clients at the same time. if the router is crowded, connections may delay or drop. connections by LTE is relatively stable and trustful.
