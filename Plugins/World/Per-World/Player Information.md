     certain player data points must be tracked and stored.  
     These are all stored in the following way:
      
        per player,
        per storyline per player,
        per world per storyline per player,
        per excursion per world per storyline per player

      tracked data:
                    
          LOCATION
          INVENTORY
          PLAYER DATA
            - exp
            - health
            - food
            - saturation
            - exhaustion
            - air
            - fireticks
            - walkspeed
            - active potion effects
                - name
                - duration
                - amplifier
                - isAmbient
                - hasParticles
                - Color (if it has one)
          
          TOTAL TIME SPENT (ticks)
          TIME LAST ENTERED
          TIME LAST LEFT

          KILL/DEATH:
            (ANY PLAYER) ----------------
                - last kill
                    - time
                    - time since previous
                    - victim uuid, name
                - last death
                    - time
                    - time since previous
                    - killer uuid, name     
                - # kills
                - # deaths
            (EACH PLAYER) ----------------
                - last kill
                    - time
                    - time since previous
                    - your k/d at the time
                    - their k/d at the time
                - last death
                    - time
                    - time since previous
                    - your k/d at the time
                    - their k/d at the time      
                - # kills
                - # deaths
          
          ?
