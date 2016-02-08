# PHP Identity and Data Security
> by: [Jonathan LeBlanc][1]

## Preface

### Attack Methods & Protection

* Brute Force Attacks
  * Protect via: Key stretching, CAPTCHA, 2FA
* Dictionary Attacks
  * Protect via: Salting
* Rainbow Tables
  * Protect via: Salting

### Considerations when salting

* Storing salts
  * Store along the hash
* Salt reuse
  * Salts should be unique
* Salt length
  * Same size as hash? 64/128 bits?

### Algorithms

* bcrypt
  * Blowfish cypher, CPU & RAM intensive
* PBKDF2
  * Performs the HMAC (hash + key)
* scrypt
  * Designed to make it costly to perform large scale (requires large amounts of memory)


[1]: https://twitter.com/jcleblanc
