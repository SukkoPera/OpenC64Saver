## OpenC64Saver

OpenC64Saver is an Open Hardware implementation of the [Computer Saver device developed by Ray Carlsen](http://personalpages.tds.net/~rcarlsen/cbm/c64/SAVER/saver.txt), mainly targeted at Commodore 64 users, but also usable on VIC-20 computers.

![Board](https://raw.githubusercontent.com/SukkoPera/OpenC64Saver/master/doc/render-top.png)

### Summary
> This over-voltage protection unit is designed to prevent damage to
the Commodore 64 computer due to a failing power supply. One of the ways
the Commodore "brick" power supply can fail is from a shorted internal
5 volt regulator. That fault puts excessive voltage into the computer
and damages chips such as RAM very quickly... and silently. The Saver
protector is essentially a fast-acting electronic circuit breaker. It
functions to quickly cut off the 5 volt supply line to the computer if
the voltage exceeds about 5.4 volts. It is not a "crowbar" device but
opens the line from the supply to the computer before the voltage gets
high enough to do damage. That's the safest way to do it. After-market
power supplies, even switching types, can fail at any time. Switchers
are more reliable and much less prone to catastrophic failures but can
still cause damage to the computer if they fail. This Saver is designed
to protect any computer that uses the standard Commodore "brick" power
supply as well as any newer switch-mode PS. Computers include all
versions of the C64, the later CR version of the VIC20, and the Plus/4.
Because of its square power connector, an external Saver is possible
for the Plus/4 but its power socket would have to be changed to the
round C64 version because four pin square DIN connectors are not
available. - Ray Carlsen

### Installation
> There are several ways to add this protection device to your system.
One way is to install the components or a completed module inside the
computer. That way, it is protected from any supply plugged into it. If
you have more than one computer, a protector can be installed in each
one. To install the protector circuit inside a C64, it is necessary to
open the +5 volt line on the circuit board. Input and output lines of
the protector are wired to each end of the now-open circuit. If your
C64 board differs from the pictures on my site, you will have to locate
the correct area of your board to open the line and make the connections.
In all internal versions, the correct point is electrically between the
power connector and the power switch. There are at least five board
versions of that computer, each with a different PC board layout, and
the physical connections will be specific for each board.

Ray's C64 motherboard pictures can be found at http://personalpages.tds.net/~rcarlsen/cbm/c64/SAVER/MOBOs/.

For the VIC-20 see [this](http://personalpages.tds.net/~rcarlsen/cbm/vic20/VIC20CR/saver%20mod.jpg). Note that you will have to cut a trace.

### Configuration
OpenC64Saver includes a trimmer to set the cut-off voltage:

> Because of fairly wide Saver component tolerances and to
accommodate the normal voltage variations of even good power supplies,
the basic Saver circuit must be "trimmed" so the voltage cuts off at
about 5.4 volts DC. If set too high, it will not protect the computer;
if too low it will trip prematurely even with a good PS. Feedback from
a few users indicated the Saver would trip when they turned their
computer off, and it remained in failsafe mode until unplugged from the
PS. Apparently some power supplies output can jump up past the failsafe
point when the load on them is suddenly removed (computer off). That's
why the trip point is set as high as it is. 5.4 volts is still under
the "absolute maximum rating" specification for the RAM chips.

To properly set the cut-out voltage you will need a variable DC supply and a voltmeter:
- Slowly increase the supply voltage until you hear the relay cut in (voltage appears on the relay output side)
- Continue advancing it until the relay cuts out again. The voltage at that instant is the trip point of the device.
- If it is too high, decrease the supply voltage until the relay cuts in again, rotate the trimmer screw, and repeat the above procedure.

> Note that the Zener diode is somewhat temperature sensitive. If very cold, the
trip point will read high, and if hot from soldering, the trip point will be low. Therefore, the mounting of the Saver components, if inside the computer, should be away from all heat producing components.

### License
OpenC64Saver is Open Hardware. If you make any modifications to the board, please contribute them back.

### Disclaimer
OpenC64Saver is provided to you 'as is' and without any express or implied warranties whatsoever with respect to its functionality, operability or use, including, without limitation, any implied warranties of merchantability, fitness for a particular purpose or infringement. We expressly disclaim any liability whatsoever for any direct, indirect, consequential, incidental or special damages, including, without limitation, lost revenues, lost profits, losses resulting from business interruption or loss of data, regardless of the form of action or legal theory under which the liability may be asserted, even if advised of the possibility or likelihood of such damages.

### Support the Project
Since the project is open you are free to get the PCBs made by your preferred manufacturer, however in case you want to support the development, you can order them from PCBWay through this link:

[![PCB from PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/OpenC64Saver_V4.html)

You get my gratitude and cheap, professionally-made and good quality PCBs, I get some credit that will help with this and [other projects](https://www.pcbway.com/project/member/shareproject/?bmbid=41100). You won't even have to worry about the various PCB options, it's all pre-configured for you!

Also, if you still have to register to that site, [you can use this link](https://www.pcbway.com/setinvite.aspx?inviteid=41100) to get some bonus initial credit (and yield me some more).

Again, if you want to use another manufacturer, feel free to, don't feel obligated :). But then you can buy me a coffee if you want:

<a href='https://ko-fi.com/L3L0U18L' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi2.png?v=2' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

### Get Help
If you need help or have questions, you can join [the official Telegram group](https://t.me/joinchat/HUHdWBC9J9JnYIrvTYfZmg).
