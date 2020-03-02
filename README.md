# Scale Workshop

![Scale Workshop screenshot](https://raw.githubusercontent.com/SeanArchibald/scale-workshop/master/src/assets/img/scale-workshop-og-image.png)


## Description

[Scale Workshop](http://sevish.com/scaleworkshop/) allows you to design microtonal scales and play them in your web browser. Export your scales for use with VST instruments. Convert Scala files to various tuning formats.


## Frequently Asked Questions

### What kinds of microtonal scales are possible with Scale Workshop?

Scale Workshop can play any kind of microtonal scale, such as equal temperaments, just intonation, historical and traditional scales, non-octave scales, and any arbitrary tunings. The application offers a few methods to generate scales automatically based on parameters you set, or otherwise you can enter your scale data manually.

### Can I play and hear my scale?

Yes, the built-in synth allows you to play your scales within the web browser. If your browser supports web MIDI then you can use a connected MIDI device to play notes. Otherwise you can use your computer keyboard (e.g. a QWERTY keyboard) as an isomorphic keyboard controller to hear your scales. You can also play on a touch device using the 'Touch Keyboard' feature.

### Can I use Scale Workshop to tune up other synths?

Scale Workshop supports any synth that uses Scala (.scl/.kbm) files or AnaMark TUN (.tun) files. It can also export Native Instruments Kontakt tuning scripts, Max/MSP coll tuning tables and Pure Data text tuning tables.

The Xen Wiki has a [list of microtonal software plugins](https://en.xen.wiki/w/List_of_Microtonal_Software_Plugins) that support Scala and AnaMark files.

### How do I enter scale/tuning data manually?

Scale data should be entered in to the large text field labeled ‘Scale data’. Add each note on its own new line. Cents and ratios are both supported.

* To specify a ratio, simply write it in the format e.g. `3/2`
* To specify an interval in cents, include a . in the line e.g. `701.9` or `1200.`
* To specify n steps out of m-EDO, write it in the format `n\m`

No need to enter `0.` or `1/1` on the first line as your scale is automatically assumed to contain this interval.

The interval on the final line is assumed to be your interval of equivalence (i.e. your octave or pseudo-octave).

Don't add any other weird data to a line. Don't try to mix decimals with ratios (e.g. `2/1.5`). Scale Workshop will try to gracefully ignore any rubbish that you put in, but it's very possible that weird stuff will happen.

### Can I copy and paste the contents of a Scala file (.scl) directly into the 'Scale data' field?

Scala files contain non-tuning related comments at the top of the file, so Scale Workshop will throw an error if you try to paste them in directly. Instead you can use the ‘Load .scl’ function, which automatically removes those comments for you. Or you can paste the Scala file but remove the comments manually.

### Can I convert a TUN file to another format?

Yes, start by clicking New > Import .TUN and then load your TUN file into Scale Workshop. Then click Export and select your desired output format. Note that Scale Workshop is not a fully compliant AnaMark TUN v2 parser, however it should be able to read TUN files exported by Scala and Scale Workshop.

### How do I make my own keyboard mapping?

Keyboard mappings are not currently supported. You can still export a Scala keyboard mapping file (.kbm) but it will assume a linear mapping.
However you can always use duplicate lines in your tuning in order to skip any keys that you don't want to include, or write your .kbm file manually.

### Can I undo/redo?

Use your browser's Back/Forward navigation buttons to undo/redo changes to your tuning.

### How can I share my tunings with a collaborator?

Use Export > Share scale as URL. The given URL can be copied and pasted to another person. When they open the link they will see a Scale Workshop page with your scale already tuned in.

### How can I save my work for later?

You can bookmark the current page to save your work for later. This works because your tuning data is stored within the bookmarked URL.

### When I export a tuning, I get a weird filename, why?

Exporting a file with the correct filename is not supported in Safari (iOS and macOS). You can try to use Firefox, Chrome or Opera instead.

### Can I run this software offline?

You can run it only, if you have a local webserver installed to your computer (https://developer.mozilla.org/en-US/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server)

### Can you add a new feature to Scale Workshop?

Probably! Just add your feature request to the [issue tracker](https://github.com/SeanArchibald/scale-workshop/issues) on GitHub.

### I found a bug

Please [create a bug report](https://github.com/SeanArchibald/scale-workshop/issues) detailing the steps to reproduce the issue. You should also include which web browser and OS you are using.

## Contributing

Please base any work on develop branch, and pull requests should also be made against develop branch not master.

## Contributors

* Sevish
* Scott Thompson
* Lajos Mészáros
* Carl Lumma
* Tobia
* Vincenzo Sicurella
