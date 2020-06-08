For augmenting a dataset: Tile, mirror and rotate .JPG and Pascal VOC .XML files by batch

Should also work for other image types, if the .JPG tags are replaced.  

NB: .jpg != .JPG, pythonwise.

Tiling functions assume all photos in the batch have the same dimensions.  Tiling differently sized images will result in odd-sized tiles at two edges, whilst the .xml tiling code will need updating to parse the relevant from inside the file itself.

Tiles without objects can be auto-removed from the dataset.

Mirror and rotate functions are size agnostic.

Mirroring a 4-fold-symmetrical set of clockwise rotations gives the anticlockwise rotations (For a gven rotation angle). And requires less reworking of the rotation function.
