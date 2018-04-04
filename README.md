![Brofist Logo](/src/qt/res/icons/bitcoin.png)

BROFIST COIN - A COMMUNITY RE-DESIGNED COIN 

What is BroFist?
----------------

This is just another one coin that the developer had gone away, and left it to be a shit coin.
Therefore, I make this fork to look after it, and make it to be the community stable and reliable coin.

* Website: http://brofist-coin.firebaseapp.com  (comming soon)
* Exchange: https://graviex.net/markets/pewbtc
* Discord: https://discord.gg/p2rsNEb

Downloads
----------------
* [Windows 64 Wallet](https://github.com/modcrypto/brofist/releases/download/1.0/brofist64-qt.zip)
* Windows 32 Wallet
* [Linux Wallet](https://github.com/modcrypto/brofist/releases/download/1.0/brofist_ubuntu.16.04.tar.gz)
* MacOS Wallet
* [Blockchain](https://github.com/modcrypto/brofist/releases/download/1.0/brofist_blockchain_24176.zip) 1 - 24176 blocks

How to Repair Your Masternode
------------------------
1. Close your BroFist wallet.
2. Delete everything from the folder <USER_FOLDER>\AppData\Roaming\BroFistCore (for windows), 
   EXCEPT wallet.dat, brofist.conf, masternode.conf and backup folder.

![Sample Screen](/doc/brofist_doc/step1.png)

Be extremely careful not to delete wallet.dat, or you may loose all your coins.

3. Then you need to add nodes that are 100% sure on the right chain to your brofist.conf file :
Code:

maxconnections=80
addnode=80.64.131.245
addnode=80.64.131.246
addnode=176.57.208.60
addnode=176.57.208.151
addnode=5.23.52.56
addnode=5.23.54.111

Please don't make maxconnections number higher than 125, or you might desync again.
4. Open your BroFist wallet again.

Master Node Guide
----------------
Coming soon


License
-------

BroFist Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is meant to be stable. Development is normally done in separate branches.
[Tags](https://github.com/brofistcoin/brofist/tags) are created to indicate new official,
stable release versions of BroFist Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](/doc/unit-tests.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`

There are also [regression and integration tests](/qa) of the RPC interface, written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/qa) are installed) with: `qa/pull-tester/rpc-tests.py`

The Travis CI system makes sure that every pull request is built for Windows
and Linux, OS X, and that unit and sanity tests are automatically run.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.
