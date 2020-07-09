# Windows 3.x Plotter Fonts

Microsoft Windows used to ship with mono-line vector fonts meant for
pen plotters. This is an archive of these files, along with sample
output.

## Original Files

`modern.fon`, `roman.fon` and `script.fon` are the Microsoft Windows font
binaries from Windows 3.11. They were originally dated 1993-10-31 and
contain the following copyright message:

    Copyright © Microsoft Corp. 1991-1992

* Modern is a sans-serif font

* Roman is a serif font

* Script is a North American cursive font.

All of the glyphs are built up from straight line segments, as simple
vector output devices could not render spline curves directly.

These files are not directly useful to today's user.

## Generated Files

Using a VM, a Windows 3.11 instance was started. A simple text file
was generated containing character codes 32 to 255 separated into 8
columns:

     	!	"	#	$	%	&	'
    (	)	*	+	,	-	.	/
    0	1	2	3	4	5	6	7
    8	9	:	;	<	=	>	?
    @	A	B	C	D	E	F	G
    ...

This was loaded into [Microsoft
Write](https://en.wikipedia.org/wiki/Microsoft_Write) and styled in
each of Modern, Roman and Script at 18 point. These files were then
output to file via Windows printer drivers:

* **PostScript** — using PSCRIPT.DRV, generating `modern18.ps`,
  `roman18.ps` and `script18.ps`

* **HP-GL** — using the HP plotter driver (most likely for an HP
  [7550](http://hpmuseum.net/display_item.php?hw=75)), generating plain
  text [HP-GL](https://en.wikipedia.org/wiki/HP-GL) files
  `modern18.plt`, `roman18.plt` and `script18.plt`.

## Derived files

* **PDF** — the PostScript files were used to generate PDF files using
  [Ghostscript](https://www.ghostscript.com/)'s `ps2pdf12` command
  
* **PNG** — raster images at 600 dpi were created from the PDF files
  using [Glyph & Cog](http://www.glyphandcog.com/)'s `pdftoppm` tool

* **SVG** — vector files were created from the PDF files using
  `pdftocairo`, again from [Glyph & Cog](http://www.glyphandcog.com/).
  
## Made by

Stewart Russell, scruss.com — 2020-07

## Licence

Except for the FON files (which remain Copyright © Microsoft
Corp. 1991-1992), you can use these files under the Creative Commons
[Attribution 4.0 International — CC BY
4.0](https://creativecommons.org/licenses/by/4.0/) licence.
