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

# Coin Specifications:
Name: 1X2COIN</br>
Ticker: 1X2</br>
Algorithm: HashX11</br>
Maximum Supply: 21,000,000 1X2_COIN</br>
Port=9214</br>
Rpcport=9213 (Default)</br>
Masternode Reward: 80%</br>
Staking Reward: 20%</br>
Masternode collateral:  1000 1X2_COIN</br>
Block Time: ~ 60 seconds</br>
Minimum staking age: 80 confirmations</br>

# reward structure
|***Block Phase*** |***Block***         | ***Reward*** | ***MN Reward(95%)*** | ***POS Reward(5%)*** | ***Collateral*** |
|------------------|--------------------|--------------|----------------------|----------------------|------------------|
| 1                | 1                  | 1            | 0.95                 | 0.05                 | 1000             |
| 2                | 15000              | 1.25         | 1.19                 | 0.06                 | 1000             |
| 3                | 22000              | 1.5          | 1.43                 | 0.08                 | 1000             |
| 4                | 29000              | 1.75         | 1.66                 | 0.09                 | 1000             |
| 5                | 36000              | 2            | 1.90                 | 0.1                  | 1000             |
| 6                | 43000              | 2.25         | 2.14                 | 0.11                 | 1000             |
| 7                | 50000              | 2.5          | 2.38                 | 0.13                 | 1000             |
| 8                | 57000              | 2.75         | 2.61                 | 0.14                 | 1000             |
| 9                | 64000              | 3            | 2.85                 | 0.15                 | 1000             |
| 10               | 71000              | 3.25         | 3.09                 | 0.16                 | 1000             |
| 11               | 78000              | 3.5          | 3.33                 | 0.18                 | 1000             |
| 12               | 85000              | 3.75         | 3.56                 | 0.19                 | 1000             |
| 13               | 92000              | 4            | 3.8                  | 0.2                  | 1000             |
| 14               | 99000              | 4.25         | 4.04                 | 0.21                 | 1000             |
| 15               | 106000             | 4.5          | 4.28                 | 0.23                 | 1000             |
| 16               | 113000             | 4.75         | 4.51                 | 0.24                 | 1000             |
| 17               | 120000             | 5            | 4.75                 | 0.25                 | 1000             |
| 18               | 127000             | 5.25         | 4.99                 | 0.26                 | 1000             |
| 19               | 134000             | 5.5          | 5.23                 | 0.28                 | 1000             |
| 20               | 141000             | 5.75         | 5.46                 | 0.29                 | 1000             |
| 21               | 148000             | 6            | 5.70                 | 0.3                  | 1000             |
| 22               | 155000             | 6.25         | 5.94                 | 0.31                 | 1000             |
| 23               | 162000             | 6.5          | 6.18                 | 0.33                 | 1000             |
| 24               | 169000             | 6.75         | 6.41                 | 0.34                 | 1000             |
| 25               | 176000             | 7            | 6.65                 | 0.35                 | 1000             |
| 26               | 183000             | 7.25         | 6.89                 | 0.36                 | 1000             |
| 27               | 190000             | 7.5          | 7.13                 | 0.38                 | 1000             |
| 28               | 197000             | 7.75         | 7.36                 | 0.39                 | 1000             |
| 29               | 204000             | 8            | 7.6                  | 0.4                  | 1000             |
| 30               | 211000             | 8.25         | 7.84                 | 0.41                 | 1000             |
| 31               | 218000             | 8.5          | 8.08                 | 0.43                 | 1000             |
| 32               | 225000             | 8.75         | 8.31                 | 0.44                 | 1000             |
| 33               | 232000             | 9            | 8.55                 | 0.45                 | 1000             |
| 34               | 239000             | 9.25         | 8.79                 | 0.46                 | 1000             |
| 35               | 246000             | 9.5          | 9.03                 | 0.48                 | 1000             |
| 36               | 253000             | 9.75         | 9.26                 | 0.49                 | 1000             |
| 37               | 260000             | 10           | 9.5                  | 0.5                  | 1000             |
| 38               | 267000             | 10.25        | 9.74                 | 0.51                 | 1000             |
| 39               | 274000             | 10.5         | 9.98                 | 0.53                 | 1000             |
| 40               | 281000             | 10.75        | 10.21                | 0.54                 | 1000             |
| 41               | 288000             | 11           | 10.45                | 0.55                 | 1000             |
| 42               | 295000             | 11.25        | 10.69                | 0.56                 | 1000             |
| 43               | 302000             | 11.5         | 10.93                | 0.58                 | 1000             |
| 44               | 309000             | 11.75        | 11.16                | 0.59                 | 1000             |
| 45               | 316000             | 12           | 11.4                 | 0.6                  | 1000             |
| 46               | 323000             | 11.75        | 11.16                | 0.59                 | 1000             |
| 47               | 330000             | 11.5         | 10.93                | 0.58                 | 1000             |
| 48               | 337000             | 11.25        | 10.69                | 0.56                 | 1000             |
| 49               | 344000             | 11           | 10.45                | 0.55                 | 1000             |
| 50               | 351000             | 10.75        | 10.21                | 0.54                 | 1000             |
| 51               | 358000             | 10.5         | 9.98                 | 0.53                 | 1000             |
| 52               | 365000             | 10.25        | 9.74                 | 0.51                 | 1000             |
| 53               | 372000             | 10           | 9.5                  | 0.5                  | 1000             |
| 54               | 379000             | 9.75         | 9.26                 | 0.49                 | 1000             |
| 55               | 386000             | 9.5          | 9.03                 | 0.48                 | 1000             |
| 56               | 393000             | 9.25         | 8.79                 | 0.46                 | 1000             |
| 57               | 400000             | 9            | 8.55                 | 0.45                 | 1000             |
| 58               | 407000             | 8.75         | 8.31                 | 0.44                 | 1000             |
| 59               | 414000             | 8.5          | 8.08                 | 0.43                 | 1000             |
| 60               | 421000             | 8.25         | 7.84                 | 0.41                 | 1000             |
| 61               | 428000             | 8            | 7.6                  | 0.4                  | 1000             |
| 62               | 435000             | 7.75         | 7.36                 | 0.39                 | 1000             |
| 63               | 442000             | 7.5          | 7.13                 | 0.38                 | 1000             |
| 64               | 449000             | 7.25         | 6.89                 | 0.36                 | 1000             |
| 65               | 456000             | 7            | 6.65                 | 0.35                 | 1000             |
| 66               | 463000             | 6.75         | 6.41                 | 0.34                 | 1000             |
| 67               | 470000             | 6.5          | 6.18                 | 0.33                 | 1000             |
| 68               | 477000             | 6.25         | 5.94                 | 0.31                 | 1000             |
| 69               | 484000             | 6            | 5.70                 | 0.3                  | 1000             |
| 70               | 491000             | 5.75         | 5.46                 | 0.29                 | 1000             |
| 71               | 498000             | 5.5          | 5.23                 | 0.28                 | 1000             |
| 72               | 505000             | 5.25         | 4.99                 | 0.26                 | 1000             |
| 73               | 512000             | 5            | 4.75                 | 0.25                 | 1000             |
| 74               | 519000             | 4.75         | 4.51                 | 0.24                 | 1000             |
| 75               | 526000             | 4.5          | 4.28                 | 0.23                 | 1000             |
| 76               | 533000             | 4.25         | 4.04                 | 0.21                 | 1000             |
| 77               | 540000             | 4            | 3.8                  | 0.2                  | 1000             |
