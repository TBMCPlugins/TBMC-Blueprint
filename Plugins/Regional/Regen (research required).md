
                1) OVERVIEW:

Intercept chunk load and save events, at the NMS level.
Decide which LAYER's version of the chunk to load from, and save to.
  
  Layers are like additional region folders, storing alternate
  versions of the world.  





                2) LAYERS:


  SEED: 
  the unmodified, from-seed version of each chunk
  stored and NEVER CHANGED.
  
  
  MODIFIED LAYER: 
  multiple modified versions of the world
  these can be associated with regions       
      
      
    DEFAULT LAYERS:
      
      
      WILDERNESS BUILD LAYER:
      temporary changes made to the wilderness are stored here.
      these chunks are periodically overwritten from SEED
      
      
    OUR LAYERS:
      
      
      "SERVER BUILD" LAYER
      this layer contains Spawn, the dungeon-portal chunks, 
      anything that is "part of the server"
      
      
      TOWN LAYER:
      this is the layer containing the stable, "official" peacetime contents of towns.
      permanent changes, made by residents, are saved here.
      
      
      OTHER:
            
            
            SOFT CLAIMS LAYERS: 
            every soft claim generates its own temporary layer
            
            
            TEMPORARY MOVECRAFT PARKING:
            want to park your craft without it being regenned to wilderness?
            
            
            WILDERNESS EVENT REGIONS:
            used for longer events taking place in the wilderness
            maybe used for pitched battles?





                3) LOGIC

 
  REGION MANAGER:
  region manager .yml declares which regions are working off which layers.
  also declares any automated chunk regeneration (and which layer to regenerate from)
  
  
  COMMAND MANAGER:
  create commands for complex actions (such as toggling war) that have multiple steps.
  possible steps: create or delete layers, or, modify settings in the region manager 
  
  
  COMMAND SCHEDULER:
  put a command on a clock





                4) HOW WE WOULD USE THIS PLUGIN:


  WAR:
  During war, affected regions are placed in SANDBOX MODE. 
  We create a temporary layer; war chunks are saved to, and loaded from, this temporary layer.
  When war ends, the temporary layer is discarded. Return to using the TOWN LAYER.


  WILDERNESS:
  Changes made to the widerness are stored in the WILDERNESS BUILD LAYER.
  When a chunk has not been modified for a while, it is reset from SEED.
  
