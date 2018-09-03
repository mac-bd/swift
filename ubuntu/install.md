## Swift Ubuntu Install

* Install Dependent Package
```sh
sudo apt-get install clang libicu-dev
```

* Download Files
1. swift-VERSION-PLATFORM.tar.gz
2. swift-VERSION-PLATFORM.tar.gz.sig

* Import PGP Keys
```sh
wget -q -O - https://swift.org/keys/all-keys.asc | \
  gpg --import -
```

* Verify PGP signature
```sh
gpg --keyserver hkp://pool.sks-keyservers.net --refresh-keys Swift

wget -q -O - https://swift.org/keys/automatic-signing-key-2.asc | \
  gpg --import -

gpg --verify swift-<VERSION>-<PLATFORM>.tar.gz.sig
```

* Extract the archive and add PATH Variable
```sh
tar xzf swift-<VERSION>-<PLATFORM>.tar.gz
export PATH=/path/to/usr/bin:"${PATH}"
```

## Swift REPL
```sh
import Foundation
1 + 1 [$R0: Int = 2]
```
