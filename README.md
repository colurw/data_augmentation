For augmenting an image recognition dataset: tile, mirror and rotate .JPG and Pascal VOC .XML files by batch.

Tiles without objects can be auto-removed from the dataset.

A validation dataset can be separated out if necessary.

File pairs should have matching filenames, i.e:  Ball.JPG, Ball.xml, image_25.JPG, image_25.xml... and be saved in the same folder.

Should also work for other image types, if the .JPG tags in the code are replaced.  

NB: .jpg != .JPG in python.

Both tiling functions assume all photos in the batch have the same dimensions.  Tiling differently sized images will result in odd-sized tiles on two edges, whilst the .xml tiling code will need updating to parse the relevant dimensions from inside the parent .xml file.

Mirror and rotate functions are size agnostic.

Mirroring a 4-fold-symmetrical set of clockwise rotations gives the equivalent anti-clockwise rotations, for a given angle.

To increase size of bounding boxes (to avoid clipping edges of rotated objects) use setting:  circular_objects = False  
