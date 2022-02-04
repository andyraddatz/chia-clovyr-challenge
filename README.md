# chia-clovyr-challenge

Sadly I ran out of time to create something functional, but I had fun anyways and the gist of my idea and what's left to implement is below. 

I'd like to give the feedback that the wide open challenge prompt is going to heavily favor people that had Chialisp projects already in progress, which kind of defeats the purpose of the 24 hour time limit.  Just something to consider in the future, I appreciate all of the effort the Chia and Clovyr teams put into this challenge no matter what!

## Project: Marmot Society Democracy by Proxy

Marmot society strives for democratic rule and wants every marmot's input to make decisions. Marmots may vote directly on every issue if they like, but may also delegate their vote to a different marmot that they trust to make good decisions on a particular issue.

Each issue that arises has a deadline for a decision to be made.  At that time, the marmot leaders will tally the votes and announce the winning option. Up until the deadline, marmots should be able to change their minds about either voting directly themselves or to which other marmot they will trust their vote.
  
This system is similar to human politics, except that any given marmot may only wield power issue-by-issue instead of being elected for a period of time where they can make decisions on every type of issue, whether or not they are qualified.  And when a marmot considers themself the expert on a particular issue they may vote directly instead of giving up their power for all issues.

Marmots should be able to commit their votes to options or proxies anonymously.

## Description of planned implementation in Chia

To enable the democratic process described above, the marmots will use the Chia blockchain. They create a single-issuance CAT for each societal issue to be voted on and distribute one CAT to every marmot's public wallet address.  Each marmot is an eligible voter and may also create a Singleton to collect CATs representing votes that they have the power to cast on others' behalf.

For each societal issue, a set of Singletons are created to represent all of the eligible options for moving forward. In addition, each issue will have its own deadline for votes to be cast via CATs paid to the respective options' Singletons. After the deadline marmot society will adopt the option for whichever Singleton has the greatest CAT amount balance.

After the CATs have been distributed, marmots may spend their CAT to a Singleton representing one of the options in order to vote directly, or spend it to the democtratic proxy Singleton that gives their trusted 3rd party marmot the power to spend their CAT to vote on their behalf.

I had not yet worked out how to implement anonymity but I believe some simple aggregate BLS signatures would be involved.  I also had not worked out where the ASSERT_BLOCK_HEIGHT_RELATIVE should go to enforce the deadlines for societal issues.

## Progress Made

Basically I made a few `.clsp` files and copied the puzzles from the Single Issuance CAT and Pooling Member puzzles, and only got to making minor first tweaks.  I think that no matter what I will continue and try to make this functional since it's an idea I've had for a long time, but Chia is the first blockchain that feels capable to truly support it.

THANK YOU CHIA AND CLOVYR TEAMS!!
