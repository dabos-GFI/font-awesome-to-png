Font Awesome to PNG
===================

This program allows you to extract the awesome
[Font Awesome] (http://fortawesome.github.com/Font-Awesome/) icons as PNG images
of specified size.

### Usage

    font-awesome-to-png.py [-h] [--color COLOR] [--filename FILENAME]
                           [--font FONT] [--css CSS] [--list] [--size SIZE]
                           [--width WIDTH] [--height HEIGHT] icon [icon ...]

    positional arguments:
      icon                 The name(s) of the icon(s) to export (or "ALL" for
                           all icons)

    optional arguments:
      --color COLOR        Color (HTML color code or name, default: black)
      --filename FILENAME  The name of the output file (it must end with
                           ".png"). If all files are exported, it is used as a
                           prefix.
      --font FONT          Font file to use (default: fontawesome-webfont.ttf)
      --css CSS            Path to the CSS file defining icon names (instead of
                           the predefined list)
      --list               List available icon names and exit
      --size SIZE          Font size in pixels (default: 16)
      --width WIDTH        Icon width in pixels (default: auto)
      --height HEIGTH      Icon height in pixels (default: auto)

    hidden optional arguments:
     --list-update         List available icon names and codes in format suitable
                           for updating the program source.

To use the program, you need a Font TTF file.

The internal icon list is matched to Font Awesome 4.1.0.  To use a later/different
version, use css option.

### Examples

Export the "play" and "stop" icons as 24x24 pixels images:

    font-awesome-to-png.py --size 24 --width 24 --height 24 play stop

Export the asterisk icon as 32x32 pixels image, in blue:

    font-awesome-to-png.py --size 32 --width 32 --height 32 --color blue asterisk

Export all icons as 16 pixels font size images:

    font-awesome-to-png.py ALL
