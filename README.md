# chia-clovyr-challenge

Sadly I ran out of time to create something functional, but I had fun anyways and the gist of my idea and what's left to implement is below. 

I'd like to give the feedback that the wide open challenge prompt is going to heavily favor people that had Chialisp projects already in progress, which kind of defeats the purpose of the 24 hour time limit.  Just something to consider in the future, I appreciate all of the effort the Chia and Clovyr teams put into this challenge no matter what!

## Project: Marmot Society Democracy by Proxy

Marmot society strives for democratic rule and wants every marmot's input to make decisions. Marmots may vote directly on every issue if they like, but may also delegate their vote to a different marmot that they trust to make good decisions on a particular issue.

Each issue that arises has a deadline for a decision to be made.  At that time, the marmot leaders will tally the votes and announce the winning option. Up until the deadline, marmots should be able to change their minds about either voting directly themselves or to which other marmot they will trust their vote.

## Implementation in Chia

To enable the democratic process described above, the marmots will use the Chia blockchain. They create a single-issuance CAT for each societal issue to be voted on and distribute one CAT to every marmot's public wallet address.

For each societal issue, a set of Singletons are created to represent all of the eligible options for moving forward. In addition, each issue will have its own deadline for votes to be cast via CATs paid to the respective options' Singletons. After the deadline marmot society will adopt the option for whichever Singleton has the greatest CAT amount balance.

After the CATs 

Marmots have a few choices for voting with their CATs.
Once the CATs are issued and distributed



Invariably this will lead to political debates and 

They create a CAT for each issue and distribute a single fungible token to each marmot to cast their vote by sending their CAT to a public address representing the option they support.    Final vote casting is time-locked for one month in the future after CAT issuance.  But marmots should be able to change their minds on where their vote will go in the mean time.  

To allow immediate commitment and also support changing their minds up until final vote time, each marmot commits their CATs to a singleton.

- voters
  - total population size = number of votes created for each issue
  - private key ID
  - singleton for collecting anonymous commitments
  - can cast their vote and any votes committed to their singleton
- votes
  - each voter gets one vote per issue
  - votes can be cast directly or committed to another voter's singleton
- decisions
  - the event where votes from voters are tallied to decide outcome of an issue
- issues
  - topic with options to be voted on
  - MarmotDefenseBudgetIncrease
  - MarmotUniversalHealthcare
  - MarmotFlatTax
- anonymous commitments
  - somehow anonymous
  - voters elect another voter to cast their vote for them for a particular issue

  - Singletons
    - voter proxy collectors
    - One per issue option (yes/no to be simple)
      - These 
  - CATs
    - all votes that are valid for a single issue
  - Other Smart Coins
    - issue deciders
      - 

### UX


## ideas

- jukebox
- vouchcoin actually different
- THIS bottom-up deferment voting system "proxy democracy"
    - people either vote directly, or commit their vote to someone they trust to vote in their interest
    - leads to organic politician emergence via individual vouching/committing votes to another person
    - somehow anonymize and allow changing vote or commitment at any time up until whatever decision is made
- proof-of-having-been-somewhere somehow, physical meatspace kiosks hidden in remote places or at coffee shops etc
    - perhaps encrypted data gets unencrypted while in a location
- white/blacklistcoin, can white/blacklist certain addresses from ever receiving XCH originating from this coin
- system of additive coin-based approvals
  - see https://chialisp.com/docs/common_functions#outer-and-inner-puzzles
  - assumption that "puzzle hash" can be a specific coloured coin
  - think power rangers and megazord
- ethical browser shopping extension
  - establish support chains explorer to discover who you are supporting when purchasing
    - Unilever, foreign companies, Haliburton, etc
      - if your purchases are lining billionaire piggy banks maybe you'd just like to know that at least
    - monetize ideas
      - charge xch to automate research and/or automatic purchasing
      - companies pay to be verified by x (any chia address)
        - establish authority or verility how?
        - how will we anonymize/decentralize so that companies don't corrupt us or it won't matter
- alternating, toggling CAT coin logic...  parent coin ID = certain CAT, then != certain CAT, then =...
- open DAO, cooperative organization (co-op), vote deferment

## zoom questions

- does `run` basically mean build from Chialisp -> CLVM?
- currying = passing in functions as arguments?

## notes

- existing coins can be referenced like libraries by puzhash
