## Standard Identifiers

In Stensl, standard identifiers are a broad class of identifiers used for many constructs. They are built from any unicode character except for Stensl reserved characters and spaces. They may be any string of any length built from those characters except for Stensl reserved keywords. The list of Stensl reserved characters and stensl reserved keywords can be found in Appendix 1.

For instance, the following are valid standard identifiers:

* `NewName`
* `name_123`
* `abcedfghijklmnopqrstuvwxyz`

By contrast, the following are invalid standard identifiers:

* `(newName)`
* `this%is%a%test`
* `func`
* `Hello there`
