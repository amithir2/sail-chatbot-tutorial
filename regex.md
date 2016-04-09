## . (Period)
#### Matches with anything (numbers, letters, etc.)
- '.' --> . --> MATCH
- 'a' --> . --> MATCH
- '/' --> . --> MATCH
- '0' --> . --> MATCH
- 'aa' --> . --> NO MATCH

## * (Asterisk)
#### Matches with the item before it, repeated 0 or more times
- '' --> a* --> MATCH
- 'aa' --> a* --> MATCH
- 'aaaaaaaaaaa' --> a* --> MATCH
- 'abababab' --> ab* --> MATCH
- 'aba' --> ab* --> NO MATCH

## .* (Period followed by Asterisk)
#### Matches anything
- '' --> .* --> MATCH
- 'aa' --> .* --> MATCH
- 'aaaaaaaaaaa' --> .* --> MATCH
- 'abababab' --> .* --> MATCH
- 'aba' --> .* --> MATCH

## + (Plus sign)
#### Matches with the item before it, repeated 1 or more times
- '' --> a+ --> NO MATCH
- 'aa' --> a+ --> MATCH
- 'aaaaaaaaaaa' --> a+ --> MATCH
- 'ab' --> ab+ --> MATCH
- 'abababab' --> ab+ --> MATCH
- 'aba' --> ab+ --> NO MATCH

## x|y 
#### Match if x matches or if y matches
- 'mother' --> 'mother|mom' --> MATCH
- 'mom' --> 'mother|mom' --> MATCH

## () 
#### Grouping, Can be used to get the text that matched
- 'mother' --> '(mother|mom)' --> MATCH
  - '%1' --> 'mother'
- 'mom' --> '(mother|mom)' --> MATCH
  - '%1' --> 'mom'

## Weird characters
Keep in mind that if you type certain punctuation in the regular expression, like apostrophe or question mark, you must include a backslash, '\', right before it 
- '\?'
- '\''
