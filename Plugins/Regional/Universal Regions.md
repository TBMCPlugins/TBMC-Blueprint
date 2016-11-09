Creates a file where all of the server's region selections are stored.  
####Types of Region

    BLOCK-BASED  
        each block-based region is a Boolean[x][y][z].  
        The TRUE/FALSE value represents whether the coordinate is, or is not, part of the region.
    
    COLUMN-BASED  
        each column-based region is a Boolean[x][z]
      
    CHUNK-BASED  
        each chunk-based region is a Boolean[x][z]
        (16x16 columns)
      
    REGION-BASED
        each region-based region is a Boolean[x][z]
        (32x32 chunks)

####Stored as Byte Serialization

    Each region is stored as a byte serialization representing the actual java object, the array itself.  
    You convert directly from string to object.

####Region Name as File Structure

    You might name a region "World_Nether.Towny.PeriwinkleNation.TownName.Outpost1"
    or "World.WorldGuard.Spawn"
    or "World.SoftClaim.iie.1.(120 -2453)"
    or even "World.misc.3"
    
    the file extensions might be 
      .blocks
      .columns
      .chunks
      .regions
      
####Stored in a central location

    Somewhere highly accessible to other plugins
    Maybe a loose file in plugins/
    or a standalone folder
