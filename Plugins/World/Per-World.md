the basic functionality is done
it can store and retrieve inventories, playerdata, and player locations


####THINGS I WILL ADD 
    locations, excursions, storylines, player tracking

    LOCATIONS

        world-specific, or
        categorical (ie "spawn" - every world has one)

          able to create, if you want, entire unique trees of defaults for each location category,
           to be used when a world does not have a coordinate set for the location category
           DEFAULT default is server spawn.

          A teleport command to that location can be given its own per-command defaults
           including "none" - ie, cancel the teleport if the target world has no coords set
           for that category

    
    EXCURSIONS  
    an excursion is an ongoing "visit" to a world.  
    each player can have multiple stored excursions per world  
    every excursion has its own inventory and/or data

        world-specific
        categorical

          excursion tracking: some excursions might terminate if the player dies, respawning them elsewhere,
           or, perform some other action in response to an event occuring within the excursion

    
    STORYLINES  
    a player can have multiple storylines, each one a separate path through the server, almost like multiple  
    accounts per player. There could be, for example, a utility admin storyline, a path completely separate  
    from the admin's journey as a player

        world scope: for each storyline, set which worlds are, or are not, part of the storyline.
         those worlds when entered might default you to a different storyline, or deny your entry entirely
         until you switch to an allowed storyline for that world.

    
    PLAYER TRACKING  
    certain player data points must be tracked and stored, such as last known location, last death, number of deaths, etc.  
    These are all stored in the following way:

        per player
        per storyline per player
        per world per storyline per player
        per excursion per world per storyline per player

      And the incomplete list of automatically tracked data points, tracked in the manner described above:

        LAST KNOWN LOCATION
        (PLAYER)
          LAST DEATH
          LAST KILL
          # DEATHS
          # KILLS
        (MOB) ...?
          LAST DEATH
          LAST KILL
          # DEATHS
          # KILLS


      maybe just implement a sort of "per-world scoreboards" type thing  
      allowing for arbitrary named objectives with arbitrary integer values
