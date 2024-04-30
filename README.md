# Installer

echo "Tools Git, Intellij, DataGrip, Postman, Jdk17 and Sublime"


#Check If Brew Is Installed
echo "Brew installing/updating"

if ! [ -x "$(command -v brew)" ]; then
      /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   else
     brew update
     brew upgrade
   fi
   
echo "Brew OK"

# Install Tools

echo "Tools installing"
brew install git
brew install --cask intellij-idea
brew install --cask datagrip
brew install --cask postman
brew install --cask sublime-text
echo "Tools installed"


# Clean Up Brew
brew cleanup

echo "Succesful"
