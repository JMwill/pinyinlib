# pinyinlib.el

Library for converting first letter of Pinyin to Simplified/Traditional Chinese
characters.

# Functions
## `buildRegexpChar`
`buildRegexpChar` converts a letter to a regular expression containing all the Chinese characters whose pinyins start with the letter. It accepts five parameters:

`char [noPuncP] [traditionalP] [onlyChineseP] [mixedP]`

The first parameter `char` is the letter to be converted. The latter four parameters are optional.
- If `noPuncP` is `true`: it will not convert English punctuations to Chinese punctuations.
- If `traditionalP` is `true`: traditional Chinese characters are used instead of simplified Chinese characters.
- If `onlyChineseP` is `true`: the resulting regular expression doesn't contain the English letter `char`.
- If `mixedP` is `true`: the resulting regular expression will contain both traditional Chinese characters and simplified Chinese characters.

When converting English punctuactions to Chinese/English punctuations, it
uses the following table:

| English Punctuation | Chinese & English Punctuations |
|---------------------|--------------------------------|
| .                   | 。.                            |
| ,                   | ，,                            |
| ?                   | ？?                            |
| :                   | ：:                            |
| !                   | ！!                            |
| ;                   | ；;                            |
| \\                  | 、\\                           |
| (                   | （(                            |
| )                   | ）)                            |
| <                   | 《<                            |
| >                   | 》>                            |
| ~                   | ～~                            |
| '                   | ‘’「」'                        |
| "                   | “”『』\"                       |
| *                   | ×*                             |
| $                   | ￥$                            |

## `buildRegexpString`

It is same as `buildRegexpChar`, except that its first parameter
is a string so that it can convert a sequence of letters to a regular
expression.

# Packages that Use This Library

none

# Acknowledgment

# Contribute
Contributions are always welcome. If you want to add some common pinyin related functions that might be useful for other packages, please send me a PR.