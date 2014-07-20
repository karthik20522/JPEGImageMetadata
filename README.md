XMP/IPTC/EXIF Metadata Extractor
==================

Extract EXIF, IPTC and XMP metadata from JPEG image. This is a modified version of the original EXIF.js project from https://github.com/jseidelin/exif-js

Usage

      <input id="file-input" type="file" />
      
      document.getElementById("file-input").onchange = function(e) {
            EXIF.getData(e.target.files[0], function() {
                  var exifData = JSON.stringify(this.exifdata, null, 2)
                  var iptcData = JSON.stringify(this.iptcdata, null, 2)
                  var xmpData = JSON.stringify(this.xmpdata, null, 2)

            var prettPrinter = "IPTC DATA: " + iptcData +
                   "\n\nXMP DATA: " + xmpData +
                   "\n\nEXIF DATA: " + exifData;
    
            document.getElementById('data').innerHTML = prettPrinter;          
        });
    }
