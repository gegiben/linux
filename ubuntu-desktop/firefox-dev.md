Spec: [Browser: Firefox Developer Edition;  Platform: Linux 64-bit; Language: English (US); Link: <https://download.mozilla.org/?product=firefox-devedition-latest-ssl&os=linux64&lang=en-US>]
Check link: <https://www.mozilla.org/en-US/firefox/all/desktop-developer/linux64/en-US/>
Tested on: Ubuntu Desktop 24.04
---------------------------------------------------------------------------
# "Install" the app
1. Terminal: 
    cd ~Downloads
2. Download and unpack:
    wget "https://download.mozilla.org/?product=firefox-devedition-latest-ssl&os=linux64&lang=en-US" -O Firefox-dev.tar.bz2
    sudo tar xjf Firefox-dev.tar.bz2 -C /opt/
    [Optional] rm -r Firefox-dev.tar.bz2
3. Create symlink to make it executable in Terminal
    sudo ln -s /opt/firefox/firefox /usr/local/bin/firefox-dev
4. Test on terminal
    firefox-dev
5. Creating Desktop Shortcut
    a) vi Firefox-dev.desktop
    b) #Copy-and-paste:
[Desktop Entry]
Name=Firefox-developer-edition
Exec=/usr/local/bin/firefox-dev
Icon=/opt/firefox/browser/chrome/icons/default/default128.png
comment=browser
Type=Application
Terminal=false
Encoding=UTF-8
Categories=Utility;

6. Copy to "Show Apps"
    sudo cp Firefox-dev.desktop /usr/share/applications/
   
---------------------------------------------------------------------------
# How to Update
1. Do not download from browser
2. Just follow the Step 1 and 2 on #"Install"
---------------------------------------------------------------------------
# How to Remove
Terminal (no sudo su):
sudo rm -r /opt/firefox/
sudo rm /usr/local/bin/firefox-dev
sudo rm /usr/share/applications/Firefox-dev.desktop
rm ~/Desktop/Firefox-dev.desktop
