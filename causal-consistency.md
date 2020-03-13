# Causal Consistency

Causal consistency is interesting as it's currently considered to be the upper level of consistency which is achievable from a CAP point of view for a system that maintains availability and partition tolerance. Meaning the system could be causally consistent and still be available and partition tolerant.

Causal consistency defines that causally related reads and writes are seen by every node in the same order (linearizability requires all operations seen in the order),
concurrent writes could be seen in changed order on different nodes. The well known example, is posting to a social network, a post that you hate your boss and before that action you removed the boss from your friends. The causal order being kept means the order of actions can't be changed - the boss can't get informed you hate him.
