# Introduction

This is a custom macOS keyboard input source for people who primarily
wish to use a US-english keyboard layout but need quick an easy access to
Swedish (sv-se) special characters åäö and ÅÄÖ.

I find it extremely useful when programming. US keyboard is just much better
for programming but I need quick access to special characters for communications.

The keyboard layout does the following replacements from the traditional US-en
keyboard layout:

- `“ = å (Alt + [)`
- `æ = ä (Alt + ')`
- `… = ö (Alt + ;)`
- `” = Å (Shift + Alt + [)`
- `Æ = Ä (Shift + Alt + ')`
- `Ú = Ö (Shift + Alt + ;)`

Similar to where those keys would be on Swedish (sv-se) keyboard.


# Installation

- `git clone https://github.com/acrookston/us-sv-keyboard`
- `cd us-sv-keyboard`
- `cp U.S.\ -\ SE.* ~/Library/Keyboard\ Layouts/`
- Log out and log back in
- Open System Settings -> Keyboard -> Input Sources -> Edit and add the layout

The layout declares Unicode script group 126, so macOS lists it under
**Others**, not under English.


# Compatibility

Tested on Mac OS X 10.6 through 10.9, and on macOS 26 (Tahoe).


# Troubleshooting

If the layout does not appear, macOS writes its parser errors to the unified log:

    log show --last 30m --predicate 'eventMessage CONTAINS "uchr"' --info

`U.S. - SE.icns` is an old single-size icon. If the layout still refuses to
appear, move it out of `~/Library/Keyboard Layouts/` and log in again.


# License

Free to use under MIT License. No warranty, liability etc, full details at: http://opensource.org/licenses/MIT

Let me know with a tweet if you like it: [@acr](http://twitter.com/acr).
