This is a hacked fork of libvpx used to allow encoding of files with the new
proposed HDR metadata. It will not be updated, and is only part of the effort
to bootstrap HDR support for VP9 and YouTube.

USAGE:

Just like normal, except put a file in /tmp/metadata.txt with a format like this:

    colour_format=2
    bits_per_channel=10
    chroma_subsampling=1
    colour_range=1
    eotf=1
    maxcll=2000
    maxfall=800
    mastering=0.68,0.32,0.265,0.69,0.15,0.06,0.314,0.351,0,2000

The meaning of the enums like 'colour_format' is still in flux, so these new
headers are useless for anything except, say, a device maker wanting to get a head
start on preparing firmware that supports the new elements for using VP9 in an
existing HDR10 workflow.

If you got your format right, the encoder will print these values back at you
when it starts.
