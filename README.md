# hng-kiridashi-data

This is a dataset that describes the coordinates and character
information of each glyph-image extracted from some full-text images
published on the Internet using the IIIF API corresponding to the
source of the HNG dataset.


## Format

Each data file consists of a header and a body.

### Header

The header consists of comment lines starting with #, and consists of
a metadata section and a column description section.

The metadata section is described in the following format:

	#<SPACE><item name><TAB>=<SPACE><value>

Currently, **manifest**, **HNG code** and **HNG source ID** are
defined as <item name>.

- **manifest**: Manifest URI of IIIF Presentation API
- **HNG code**: HNG folder code of the source
- **HNG source ID**: HNG ID of the source

Column description section is the following format:

	# osid	sid	page	ln	cn	x	y	w	h	char	hng-gid	flg	remarks	img	mx	my	canvas

It describes the name of fields.


### Body

The format of body is TSV (tab-separated values).  Each column is as
follows.

|No.|Field  |Description                                       |
----|-------|---------------------------------------------------
|1  |osid   |Original SID in Kiridashi-kun                     |
|2  |sid    |SID in Kiridashi-kun                              |  
|3  |page   |Page ID                                           |
|4  |ln     |Line Number within a page                         |
|5  |cn     |Character Number within a line                    |
|6  |x      |X coordinate of rectangle where glyph-image exists|
|7  |y      |Y coordinate of rectangle where glyph-image exists|
|8  |w      |Width of rectangle where glyph-image exists       |
|9  |h      |Height of rectangle where glyph-image exists      |
|10  |char   |Character corresponding with glyph-image          |
|11 |hng-gid|HNG glyph code of the source                      |
|12 |flg    |Glyph Variant Code; 0=not specified; 1=a, 2=b, ...|
|13 |remarks|Note                                              |
|14 |img    |Image Information Request URI of IIIF Image API   |
|15 |mx     |Image width                                       |
|16 |my     |Image height                                      |
|17 |canvas |Canvas URI of IIIF Presentation API               |


## License

This package is free software (open data); you can redistribute it
and/or modify it under the terms of [![CC BY-SA
4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png) Creative
Commons Attribution-ShareAlike 4.0 International (CC BY-SA
4.0)](http://creativecommons.org/licenses/by-sa/4.0/) or the GNU
General Public License as published by the Free Software Foundation;
either version 2, or (at your option) any later version.

This package is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

You should have received a copy of the GNU General Public License
along with this package; see the file COPYING.  If not, write to
the Free Software Foundation, Inc., 59 Temple Place - Suite 330,
Boston, MA 02111-1307, USA.
