phpThumbnailer
==============

Warning; this project is hardly deprecated, do not use it in production.

phpThumbnailer is a simple PHP class for create thumbnails or resize images.

Requirements
------------
GD extension enabled PHP.

Sample Use
----------
```
<?php
  include("class.Thumbnail.php");
  $tn_image = new Thumbnail("sample.png", 0, 0, 50, 75);
                        #      |          |  |   |   |
			#      |          |  |   |   + JPEG Quality (optional)
			#      |          |  |   +-- Percent (optional)
		        #      |          |  +-- Maximum height (optional)
		        #      |          +-- Maximum width (optional)
			#      +-- Original image filename

  # To show
  $tn_image->show();

  # To save (it won't show image)
  $tn_image->save("tn_sample.png");
  # or
  $tn_image->show("tn_sample.png");
?>

For more samples see samples/sample.html...

Note
----
Version of GD library older than gd-1.6 support GIF format images, and do not
support PNG images, where versions greather than gd-1.6 support PNG, not GIF.

In order to create thumbnails in JPEG format, you will need to obtain and
install jpeg-6b library, and then recompile gd to make use of jpeg-6b. You
will also have to compile PHP with --with-jpeg-dir=/path/to/jpeg-6b.

Disclaimer
----------
No responsiblity for any security risks or software bugs whatsoever is
accepted by the author(s).
