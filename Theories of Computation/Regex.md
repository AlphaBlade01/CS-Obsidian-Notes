$\Sigma$ - finite set of at least 2 characters
$\Sigma$* - set of all words
**language** - subset of $\Sigma$* i.e. any set of words
**regular** - A language $L \subseteq \Sigma$* that can be represented by a regex 
**compliment** - All words that aren't part of the regex
### Facts
- compliment & intersection of two regular regex sets are regular
# Regex
If $E$ & $F$ are regexes:
- $EF$ accepts any word that is a concatenation of two words
- $E|F$ accepts any words that either E accepts or F accepts
If $E$ is a regex:
- $E$* accepts any word that's the concatenation of 0 or more words
- $E$+ accepts one or more word
### Precedence
- Juxtaposition has higher precedence than $|$ and lower precedence than * 
