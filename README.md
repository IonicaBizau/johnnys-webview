
# [![BAT - Build Awesome Tools For Desktop using WEB Technologies](/resources/header.png)](http://ionicabizau.github.io/bat/)

 [![Support me on Patreon][badge_patreon]][patreon] [![Buy me a book][badge_amazon]][amazon] [![PayPal][badge_paypal_donate]][paypal-donations] [![Version](https://img.shields.io/npm/v/bat.svg)](https://www.npmjs.com/package/bat) [![Downloads](https://img.shields.io/npm/dt/bat.svg)](https://www.npmjs.com/package/bat)

> A tiny tool for building native desktop applications using WEB technologies.

## Installation
### Linux

You can compile it from source, using the scripts or, just download the latest binary using the following commands:

```sh
# Download the deb package
$ wget https://github.com/IonicaBizau/bat/raw/master/dists/deb/64bit/dev-release.deb
# And install it
$ sudo dpkg -i dev-release.deb
```
### Mac OS X

You can just download the latest binary package using the following commands:

```sh
# Download the binary package
# Using curl
$ sudo curl https://github.com/IonicaBizau/bat/raw/master/dists/osx/Bat -o /usr/bin/bat

# (OR) Using wget
$ sudo wget -O /usr/bin/bat https://github.com/IonicaBizau/bat/raw/master/dists/osx/Bat
```

If you prefer to compile it from source, execute the following command(inside `source` directory) before running the provided scripts:

```sh
# Add CONFIG -= app_bundle into Bat.pro file
$ echo "CONFIG -= app_bundle" >> Bat.pro
```
### Windows

There are no binaries available for Windows. The application needs to be compiled on Windows. Contributions are welcome! :smile:

## Help
```sh
$ bat --help
Usage: bat [options]

Options:
  -h, --help                          Displays this help.
  -v, --version                       Displays version information.
  -t, --title <title>                 Sets the window title on start.
  -s, --size <WxH>                    Sets the BAT window size.
  -d, --document <path/to/file.html>  The path to the document you want BAT to
                                      load.
  -u, --undecorate                    Starts BAT with an undecorated window.
  --tt, --tooltip                     Starts BAT with a tooltip window.
  -m, --most                          If TOP is provided, then the window is
                                      keept on the top of the other windows. If
                                      BOTTOM is provided, the window will be in
                                      the behind of all windows.
  --debug                             Starts BAT in the debug mode.
```
## Demo

![Demo](/resources/demo.png)

## JavaScript API

The following functions are implemented for the Javascript API.

<table>
  <thead>
    <tr>
      <th>Function name</th>
      <th>Arguments</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>BAT.closeWindow()</code></td>
      <td>No arguments</td>
      <td>Closes the window</td>
    </tr>
    <tr>
      <td><code>BAT.resize(width, height);</code></td>
      <td>
        <code>width</code> - the new width of the window,
        <code>height</code> - the new height of the window</td>
      <td>Resizes the window</td>
    </tr>
    <tr>
      <td><code>BAT.setWindowFlags(type)</code></td>
      <td>
        <ul>
          <li><code>UNDECORATED</code> - undecorates the window</li>
          <li><code>BOTTOM_MOST</code> - puts the window on the background</li>
          <li><code>TOP_MOST</code> - puts the window on the top</li>
          <li><code>REMOVE_MINIMIZE</code> - removes the minimize button</li>
          <li><code>REMOVE_MAXIMIZE</code> - removes the maximize button</li>
          <li><code>REMOVE_CLOSE</code> - removes the close button</li>
          <li><code>TOOLTIP</code> - converts the window in a tooltip</li>
        </ul>
      </td>
      <td>Sets the window flags</td>
    </tr>
    <tr>
      <td><code>BAT.setWindowState(value)</code></td>
      <td>One of the following values:
        <code>MAXIMIZED</code>,
        <code>MINIMIZED</code>,
        <code>FULLSCREEN</code>,
        <code>ACTIVE</code>,
        <code>RESTORED</code></td>
      <td>Sets the window state</td>
    </tr>
    <tr>
      <td><code>BAT.getWindowSize()</code></td>
      <td>No argumnets</td>
      <td>Returns an object that contains <code>width</code> and <code>height</code> fields that represent the sizes of the window.</td>
    </tr>
    <tr>
      <td><code>BAT.getWindowPosition()</code></td>
      <td>No argumnets</td>
      <td>Returns an object that contains <code>top</code> and <code>left</code> fields that represent the coordinates of the window.</td>
    </tr>
    <tr>
      <td><code>BAT.setWindowPosition(top, left)</code></td>
      <td><code>top</code> and <code>left</code> coordinates for the new position of the window</td>
      <td>Sets the new position of the window on the screen.</td>
    </tr>
    <tr>
      <td><code>BAT.getMousePosition()</code></td>
      <td>No argumnets</td>
      <td>Gets the mouse position on the screen.</td>
    </tr>
    <tr>
      <td><code>BAT.setMousePosition(x, y)</code></td>
      <td>
        <code>x</code> - the x coordinate of the mouse,
        <code>y</code> - the y coordinate of the mouse</td>
      <td>Sets the mouse position on the screen.</td>
    </tr>
    <tr>
      <td><code>BAT.debug(message)</code></td>
      <td><code>message</code>  - string that will be printed in the console</td>
      <td>Outputs a message in the terminal.</td>
    </tr>
    <tr>
      <td><code>BAT.setWindowTitle(newTitle)</code></td>
      <td><code>newTitle</code> - string that represents the new title that you want to set to the window</td>
      <td>Sets the new window title.</td>
    </tr>
    <tr>
      <td><code>BAT.inspectElement()</code></td>
      <td>No arguments</td>
      <td>Opens the BAT developer tools window.</td>
    </tr>
    <tr>
      <td><code>BAT.runBash(command)</code></td>
      <td><code>command</code> - string that represents the command that you want to run in the bash via BAT.</td>
      <td>Runs a bash command.</td>
    </tr>
    <tr>
      <td><code>BAT.getScreenSize()</code></td>
      <td>No arguments</td>
      <td>Returns an object that contains <code>width</code> and <code>height</code> fields that represent the sizes of the screen.</td>
    </tr>
  </tbody>
</table>

## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :sparkling_heart: Support my projects

I open-source almost everything I can, and I try to reply everyone needing help using these projects. Obviously,
this takes time. You can integrate and use these projects in your applications *for free*! You can even change the source code and redistribute (even resell it).

However, if you get some profit from this or just want to encourage me to continue creating stuff, there are few ways you can do it:

 - Starring and sharing the projects you like :rocket:
 - [![PayPal][badge_paypal]][paypal-donations]—You can make one-time donations via PayPal. I'll probably buy a ~~coffee~~ tea. :tea:
 - [![Support me on Patreon][badge_patreon]][patreon]—Set up a recurring monthly donation and you will get interesting news about what I'm doing (things that I don't share with everyone).
 - **Bitcoin**—You can send me bitcoins at this address (or scanning the code below): `1P9BRsmazNQcuyTxEqveUsnf5CERdq35V6`

    ![](https://i.imgur.com/z6OQI95.png)

Thanks! :heart:



## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[badge_patreon]: http://ionicabizau.github.io/badges/patreon.svg
[badge_amazon]: http://ionicabizau.github.io/badges/amazon.svg
[badge_paypal]: http://ionicabizau.github.io/badges/paypal.svg
[badge_paypal_donate]: http://ionicabizau.github.io/badges/paypal_donate.svg
[patreon]: https://www.patreon.com/ionicabizau
[amazon]: http://amzn.eu/hRo9sIZ
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(https%3A%2F%2Fionicabizau.net)&year=2013#license-mit
[website]: https://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
