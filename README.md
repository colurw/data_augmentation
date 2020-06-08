For augmenting a dataset: Tile, mirror and rotate .JPG and Pascal VOC .XML files by batch

Should also work for other image types, if the .JPG tags are replaced.  

NB: .jpg != .JPG, pythonwise.

Tiling functions assume all photos in the batch have the same dimensions.  Tiling differently sized images will result in odd-sized tiles at two edges, whilst the .xml tiling code will need updating to parse dimensions of the parent file from inside the file itself.

Tiles are numbered:  2_0   2_1   2_2
                     1_0   1_1   1_2
                     0_0   0_1   0_2   ...

Mirror and rotate functions are size agnostic.

Mirroring a 4-fold symmetrical set of clockwise rotations gives the equiavlent anticlockwise rotations, for a given angle.  
And requires less reworking of the rotation function.
