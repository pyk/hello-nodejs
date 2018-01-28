# Hello Node!

It's been a long time I don't [write program](https://github.com/pyk?utf8=%E2%9C%93&tab=repositories&q=&type=&language=javascript)
using NodeJs haha. This repository goal is to refresh my brain about
node.js, afterall this is weekend: Me time! haha


## Node Installation

I use [nvm][nvm] to manage node.js version.
Here step by step to setup my node environment:

1. Install [nvm][nvm]

        wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
        exec $SHELL
        nvm --version

2. Install the latest LTS available

        nvm install --lts=carbon --latest-npm

3. Make sure it's work

        % node --version
        v8.9.4
        % npm --version
        5.6.0

[nvm]: https://github.com/creationix/nvm



## Start new project

I will build a simple HTTP server using [micro][micro].

Install [micro][micro] using the following command:

    npm install --save micro
    npm install --save-dev micro-dev

Update `index.js`:

    module.exports = () => "Hello\n";

Update npm `scripts` in `package.json`:

    "scripts": {
        "start": "micro",
        "dev": "micro-dev"
    }

Run the server:

    % npm run dev
    > hello-nodejs@0.0.1 dev /home/pyk/go/src/github.com/pyk/hello-nodejs
    > micro-dev
       ┌───────────────────────────────────────────────────┐
       │                                                   │
       │   Micro is running!                               │
       │                                                   │
       │   • Local:            http://localhost:3000       │
       │   • On Your Network:  http://192.168.8.100:3000   │
       │                                                   │
       │   Copied local address to clipboard!              │
       │                                                   │
       └───────────────────────────────────────────────────┘

## Setu

[micro]: https://github.com/zeit/micro
