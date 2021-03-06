1X2 Coin Core (fork of PIVX) integration/staging repository
======================================


It is recommended [use the shell script](https://github.com/1x2-coin/linux-install) to install a 1X2 Coin Masternode on a Linux server running Ubuntu 14.04, 16.04, 18.04

***

Quick installation of the 1X2 Coin daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/1x2-coin/1x2coin.git 1x2coin
    cd 1x2coin
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip 1x2coind
    sudo strip 1x2coin-cli
    sudo strip 1x2coin-tx
    cd ..

Running the daemon:

    1x2coind

Stopping the daemon:

    1x2coin-cli stop

Demon status:

    1x2coin-cli getinfo
    1x2coin-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/1x2-coin/1x2coin/releases

P2P port: 9214, RPC port: 9213
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
