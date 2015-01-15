phpThumbnailer
==============

Warning; this project is hardly deprecated, do not use it in production.

phpThumbnailer is a simple PHP class for create thumbnails or resize images.

Requirements
------------
GD extension installed.

Sample Use
----------
```
<?php
include("class.Thumbnail.php");
$tn_image = new Thumbnail("sample.png", 0, 0, 50, 75);

/**
 * Parameter order:
 * 1) Original image filename
 * 2) Maximum width (optional)
 * 3) Maximum height (optional)
 * 4) Percent (optional)
 * 5) JPEG quality (optional)
 */

/**
 * To show (output is image resource)
 */
$tn_image->show();

/**
 * To save as a file.
 */
$tn_image->save("tn_sample.png");
?>
```

For more samples see samples/sample.html file.

Disclaimer
----------
No responsiblity for any security risks or software bugs whatsoever is
accepted by the author(s).
