Roles: judge (voting initiator), juries.

    Judge publishes a decision on some topic, f.e "Death sentence hearing on case #01232"
    Judge publishes M public keys of juries and number N: N <= M - amount of needed votes "for"
    Each jury:
        generates message, voting "for" judge's decision. Voting "against" is passive (just do nothing)
        generates ring-signature for this message, using public keys of other juries (under the hood)
        sends transaction with ring-signature to contract
    Contract collects each correct signature, and increases number of votes "for" if all ok
    If N votes "for" is reached, action is performed

[testnet](https://rinkeby.etherscan.io/address/0x48014ad26e51237d759f0fb4d81bfd09c4d3df7b#code)
