# full-stack-solana-development-1

Prerequisites
Node.js - I recommend installing Node using either nvm or fnm

Solana Tool Suite - You can see the installation instructions here. note - I had a very hard time getting everything working on an M1 Mac, mainly solana-test-validator and cargo-build-bpf. I finally figured it out, and posted my solution here. I'm sure at some point this will be fixed and work out of the box.

Anchor - Anchor installation was pretty straight-forward for me. You can find the installation instructions here.

Solana browser wallet - I recommend Phantom, which is what I have tested this app with.

To build
Clone the repo
git clone https://github.com/bluedragon1120/full-stack-solana-development-1.git
Change into the project directory you'd like to run

Install the dependencies

npm install
Start a local Solana node
solana-test-validator
Build the anchor project
anchor build
Fetch the project ID for the build:
solana address -k target/deploy/<programname>-keypair.json
Update the project ID in the Rust program located at projectname/programs/src/programname.rs with the output from above.

Run the tests

anchor test
Change into the app directory and install the dependencies:
cd app && npm install
Run the client-side app
npm start
