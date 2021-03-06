## Getting started with the Rascal ##

This eight minute video demonstrates web-based editing with the Rascal. It's a good place to start if you're unfamiliar with the Rascal.

<iframe class="span10" src="http://player.vimeo.com/video/31444914?title=0&amp;byline=0&amp;portrait=0&amp;color=C6433C" height="461" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

### Plugging the Rascal in ###

The Rascal needs two connections to do anything useful-- an Ethernet cable and a power cable. Plug in the Ethernet cable first so that it will be ready to go when the Rascal starts. After you plug in the power, the Rascal will take around 25 seconds to boot. It might take a little more time depending on how fast it gets assigned an IP address on your network.

As soon as the Linux kernel is up and running, the Rascal will turn off one of the green LEDs on the board (the one that is *not* next to the power jack).

After that, it will take a few seconds to start its web interface.

### The web interface ###

There's a sticker on the bottom of your Rascal that tells you the Bonjour address of your Rascal. (Bonjour is a protocol, created by Apple, used by printers to announce themselves on a network. It works natively on OS X and Linux; if you're running Windows, you'll want to install [Bonjour for Windows][1].) Your address should look something like: <code>rascal819.local</code>

Once you know your Rascal's address, you can access your Rascal's editor like this: <code>http://rascal819.local/editor</code>

After a brief stop at the login page where you enter the password that was included in the box with your Rascal, you'll find the editor.

<img src="/img/sprinkler-template-screenshot.png" width="820px">

### Troubleshooting ###

If both green LEDs remain on, try reseating your microSD card.

If the Rascal won't resolve at its Bonjour address, it's most likely that your DHCP server is failing to dole out an address. You might try using a Bonjour browser (iStumbler or Bonjour Browser for OS X, avahi-discover for Linux) to see if the address is getting broadcast. If the Rascal can't get an DHCP address, it will fall back to a link-local address.

When the Rascal boots, it sends a large amount of diagnostic data out its debug serial port and then waits for someone to login. You can connect to this serial port with 3.3 V signals at 115200 bps. The pins are arranged in order to match [Sparkfun's FTDI adapters][2] and cables. If you have a recent 5 V adapter, it can be converted to 3.3 V with the solder jumper on the bottom of the board.

[1]: http://support.apple.com/kb/DL999
[2]: https://www.sparkfun.com/products/9873

