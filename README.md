Ecoin integration/staging tree
================================

http://www.ECoin.info

Copyright (c) 2009-2013 Bitcoin Developers

Copyright (c) 2018 Ecoin Developers

What is Ecoin?
----------------

 - - Ecoin is a hybrid x11 hash algorithm
 - - 3 minute block targets
 - - 1000 coins per block and reduce 0.8 every 100000 block
 - - 12.5 coins after block 800000 
 - - subsidy halves in 34m blocks (~199 years)
 - - 60 second block targets
 - - Proof of Work
 - - Difficulty retarget is handled by KGW with the time warp patch
 - - Block Maturation - 60 Confirmations
 - - 4 Confirmations

-  For more information, as well as an immediately useable, binary version of
the ecoin client sofware, see http://www.ecoin.info

License
-------

ECoin is licensed under the MIT License. A short and simple permissive license with conditions only requiring preservation of copyright and license notices. Licensed works, modifications, and larger works may be distributed under different terms and without source code.

Development process
-------------------

As always, developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Givecoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/arkadgmx/ecoin) are created
regularly to indicate new official, stable release versions of Ecoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./Ecoin-qt_test

