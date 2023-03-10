# Information Theory

## Introduction

In information theory, and particularly the field of computer science, the standard unit of information
is the Bit. One bit can only represent either of the 2 discrete values: 1 or 0 (i.e. True or False,
respectively).

When you have more than one bit, the number of discrete values you are able to store grows exponentially.
For example, a standard signed 32-bit integer is able to represent any integer from $0$ to $2^{32}-1$.

The major goal in information theory is for the transmitter to convey some message to the receiver.
To do so, the transmitter sends a series of partial messages to give clues towards the original message.
The amount of information of the partial message can be measured by how much uncertainty the message
resolves for the reader, specifically how many times the observation space is halved. Some people also
refer to it as how "surprising" the message is. If the message does not resolve **any** uncertainty,
the no information has been transmitted.

> **Random Joke** <br>
> `A:` I flipped a coin, what side do you think it landed on? <br>
> `B:` Heads? <br>
> `A:` If you were correct, how surprised would you be? <br>
> `B:` A bit, I guess <br>
> `A:` Now, how surprised would you be if I were to flip 2 coins, and both landed on heads? <br>
> `B:` Well... perhaps a bit more <br>

## Formula

$I(x) = -\log_2(p(x))$ where $p(x)$ represents the probability of event $x$ happening.

Now, how is this formula derived, and how is information linked with probability?

Let's go back to our coin flipping joke. Flipping a coin will result in either the coin landing on heads,
or on tails - 2 possibilities, which means our observation space has 2 units. If we were told that the
coin landed on heads, then our observation space becomes 1 unit (The coin cannot be tails). As our
observation space got exactly halved, the information transmitted was exactly 1 Bit. For the case where
2 coins were flipped, our initial observation space contained 4 units or 4 possibilities
(i.e. HH, HT, TH, TT). We are told that both coins landed on heads, limiting our observation space to
only 1 unit (i.e. HH), hence 2 bits of information were transmitted as our observation space was
halved exactly twice.

As previously stated, the amount of information transmitted is number of times our observation space
got halved. Hence, we need to take the logarithm base 2 of how "useful" the information is.
Intuitively, usefulness scales inversely with probability (i.e. $1/p(x)$). Thus, we get the formula:
$I(x) = \log_2(1/p(x))$ and simplifying to get $I(x) = -\log_2(p(x))$.