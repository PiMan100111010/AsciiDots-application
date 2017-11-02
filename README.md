This is an application to open files for the [esoteric language AsciiDots](https://github.com/aaronduino/asciidots) on Apple computers without using Terminal.

The [original AsciiDots repository](https://github.com/aaronduino/asciidots#installing) recommends running programs through Terminal using:
```
python3 __main__.py [arguments]
```
Slightly faster is aliasing these first two commands to asciidots using:
```
echo "alias asciidots='python3 $(pwd)/__main__.sh'" >> ~/.bash_profile
```
For some reason I couldn't get this second version to work, and besides, both of these methods use terminal. I am exceedingly lazy, so of course I spent hours learning how to write an AppleScript so I could simply double-click a file to open it. I now present this app to you so that you can be even be more lazy than me!

Again, please note that this will only work for Apple computers.

To use this application, first download and install [AsciiDots](https://github.com/aaronduino/asciidots#installing) as recommended, using either
```
pip3 install asciidots
```
or
```
git clone https://github.com/aaronduino/asciidots
pip3 install -r requirements.txt
```
Then, download this repository as a ZIP (under green "Clone or download" button) and unzip it. Open Automator, click the Automator icon, select "Open an Existing Document...", and select the application. Change where it says "DEFAULT TERMINAL DIRECTORY" to your default Terminal directory (duh). If you don't know what this is, open Terminal. The bottom line will say `[name of computer]:~ [default directory]$`.

Then, save the Automator file and drag it from the unzipped folder into asciidots-master (the README and liscense are not necessary). Finally, right-click any .dots file and select Open With-->Other...--> Run program.app. Select "Always Open With."

Now, right-clicking any .dots file will open it! It will first prompt you to enter any [flags](https://github.com/aaronduino/asciidots#using-the-interpreter) you would like to use (if you don't want any, leave this blank), and then run the file in Terminal!
