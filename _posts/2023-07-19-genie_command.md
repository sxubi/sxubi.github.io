---
layout: post
mathjax: true
categories: media
title: "Simulating and Analyzing Neutrino Interactions via GENIE"
---

This post aims to share the author's research experience in simulating and analyzing neutrino interactions via GENIE. Since the author is still green in neutrino physics research, the following techniques might not be very accurate. The readers may refer to the [GENIE manual](https://genie-docdb.pp.rl.ac.uk/cgi-bin/ShowDocument?docid=2) for details.

### Generating Neutrino Interaction Events
To begin with, for example, we generate 20,000 events of muon-neutrino with energy 0.1 GeV interacting with Carbon 12 at rest, using the pre-computed cross-section files from Fermi Lab:
```
gevgen -n 20000 -e 0.1 -p 14 -t 1000060120 --cross-sections /THE/PATH/TO/cross-sections/gxspl-NUsmall.xml
```
The `gevgen` command would generate a ROOT file named `gntp.0.ghep.root` in the same directory. This ROOT file could be converted to other ROOT formats like `gst`, `rootracker` etc. Then we use the `gevdump` command to ouput the event records into a text file named `example.txt`:
