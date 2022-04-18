## Appendix 2: Versioning

Stensl generally uses [Semantic Versioning 2.0.0](https://semver.org/) with a few changes and simplifications. Stensl’s version number follows the grammar below:


```
<version> ::= [a]<major>.<minor>.<patch>
<major> ::= <nonzero number>
<minor> ::= <number>
<patch> ::= <number>
<nonzero number> ::= <number><digit> | <nonzero digit>
<number> ::= <digit> | <digit><number>
<nonzero digit> ::= 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
<digit> ::= 0 | <nonzero digit>
```


Where a digit is defined as an integer from 0-9. 

Stensl version numbers, as can be seen from the above grammar, are broken down into three separate numbers plus an alpha signifier. The alpha signifier, when present, designates that the version number is an “alpha version,” that it is before the main public release. This signifier takes the form of an “a” before the version number. Following that is the major version number, which is incremented for versions which break backwards compatibility from immediately previous versions. Following that is the minor version number, which is incremented for versions that introduce new features but do not break backwards compatibility. Following that is the patch number, which is incremented for all other versions (such as those that repair bugs but don’t add new features). Note that from these rules, only one of the version numbers should be incremented per version.

When comparing two versions of Stensl to find the more recent one, the following rules should be applied in order:



* If one version is alpha and the other is not alpha, the version which is not alpha is the more recent version. Otherwise, if both versions are alpha or both versions are not alpha, then proceed to the next rule
* If one version number’s major number is greater than the other’s major number, the one with the higher major number is the more recent version. Otherwise, if both are the same, then proceed to the next rule
* If one version number’s minor number is greater than the other’s minor number, the one with the higher minor number is the more recent version. Otherwise, if both are the same, then proceed to the next rule
* If one version number’s patch number is greater than the other’s patch number, the one with the higher patch number is the more recent version. 