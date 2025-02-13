# TagUI

**TagUI is a command-line tool for digital process automation (RPA).**

### Installation
There is a new dependency in newer versions of macOS. To fix the error do the following. It installs Homebrew (a package manager for macOS) and installs OpenSSL for https connections.
If you do not have Homebrew or don't know what is Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update && brew upgrade
brew uninstall openssl; brew uninstall openssl; brew install https://github.com/tebelorg/Tump/releases/download/v1.0.0/openssl.rb
```  
Or if you already have Homebrew installed
```
brew update && brew upgrade
brew uninstall openssl; brew uninstall openssl; brew install https://github.com/tebelorg/Tump/releases/download/v1.0.0/openssl.rb
```
And after executing this command
```
export LDFLAGS="-L/usr/local/opt/openssl/lib"
export CPPFLAGS="-I/usr/local/opt/openssl/include"
```
### Download
First you go to "src" directory in "TagUI"
```
cd ../tagui/src
```

#### 1. E-Way Bill : Generated By Others
##### PARAMETERS
- Add the USERNAME in the first parameter.
- Add the PASSWORD in the second parameter.
- Add a START DATE to the third parameter. (The date format should be DD/MM/YYYY)
- Add a END DATE in the fourth parameter. (The date format should be DD/MM/YYYY)
- Add a group of days in the fifth parameter. (this field is optional. Five Days is the default group.)
```
./tagui generated_by_others_by_customer/run USERNAME PASSWORD START_DATE END_DATE DAY_GROUP chrome
```
Example 1 : (without group of days parameter)
```
./tagui generated_by_others_by_customer/run admin@gmail.com admin@123 01/01/2019 20/01/2019 chrome
```
Example 2 : (with group of days parameter)
```
./tagui generated_by_others_by_customer/run admin@gmail.com admin@123 01/01/2019 20/01/2019 4 chrome
```

#### 2. E-Way Bill : Generate By Me (Outward Supplies)
##### PARAMETERS
- Add the USERNAME in the first parameter.
- Add the PASSWORD in the second parameter.
- Add a START DATE to the third parameter. (The date format should be DD/MM/YYYY)
- Add a END DATE in the fourth parameter. (The date format should be DD/MM/YYYY)
- Add a group of days in the fifth parameter. (this field is optional. Five Days is the default group.)
```
./tagui generated_by_me_by_customer/run USERNAME PASSWORD START_DATE END_DATE DAY_GROUP chrome
```
Example 1 : (without group of days parameter)
```
./tagui generated_by_me_by_customer/run admin@gmail.com admin@123 01/01/2019 20/01/2019 chrome
```
Example 2 : (with group of days parameter)
```
./tagui generated_by_me_by_customer/run admin@gmail.com admin@123 01/01/2019 20/01/2019 4 chrome
```