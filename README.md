# Phos' RegEx Patterns
A collection of useful RegEx patterns all tested with [regex101.com](regex101.com). Feel free to add your own!

# Basics
- Digits: `[0-9]+`
- Integer: `\-?[0-9]+`
- Float/integer: `\-?[0-9]+(\.[0-9]+)?`
- Letters: `[[:alpha:]]+`
- Uppercase: `[[:upper:]]+`
- Lowercase: `[[:lower:]]+`
- ASCII: `[[:ascii:]]+`
- Hexadecimal: `[[:xdigit:]]+` or `\#[[:xdigit:]]+`

# Date & time
- Date YYYY-MM-DD: `(?x) (?(DEFINE)(?'sep'\/|\-|\ )) [0-9]{4}(?&sep)([1-9](?&sep)|10(?&sep)|11(?&sep)|12(?&sep)) ([0-9]$|[0-2][0-9]|3[0-1])`
- Date MM-DD-YYYY: `(?x) (?(DEFINE)(?'sep'\/|\-|\ )) ([1-9](?&sep)|10(?&sep)|11(?&sep)|12(?&sep)) ([0-9]|[0-2][0-9]|3[0-1])(?&sep)[0-9]{4}`
- Time 12-hour: `([1-9]|10|11|12):[0-5][0-9]`
- Time 12-hour signed: `([1-9]|10|11|12):[0-5][0-9]\ ?(A|P)M`
- Time 24-hour: `([0-9]|1[0-9]|2[0-3]):[0-5][0-9]`

# Other
- Webstie URL: `(?x) ((https?:\/\/)|(www\.)) ([-a-zA-Z0-9@:%._\+~#=]{2,256} \. [a-z]{2,6}) ([-a-zA-Z0-9@:%_\+.~#()?&\/=]*)`
- Email: `(([[:alnum:]_-])|((?<!\.|^)\.))+@(?1)+` (Not perfect: doesn't enforce top-level domain name, allows "." at the beginning of the domain name & at the end of username & top-level domain name.)
