XMP/IPTC/EXIF Metadata Extractor
==================

Extract EXIF, IPTC and XMP data from JPEG image. This is a modified version of the original EXIF.js project from https://github.com/jseidelin/exif-js

Usage

      <input id="file-input" type="file" />
      
      document.getElementById("file-input").onchange = function(e) {
        EXIF.getData(e.target.files[0], function() {
            var exifData = JSON.stringify(this.exifdata)
            var iptcData = JSON.stringify(this.iptcdata)
            var xmpData = JSON.stringify(this.xmpdata)
    
        var prettPrinter = "IPTC DATA: " + JSON.stringify(JSON.parse(iptcData),null,2) + 
                       "\n\nXMP DATA: " + JSON.stringify(JSON.parse(xmpData),null,2) + 
                       "\n\nEXIF DATA: " + JSON.stringify(JSON.parse(exifData),null,2);
    
            document.getElementById('data').innerHTML = prettPrinter;          
        });
    }
