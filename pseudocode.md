# How to make a cup of coffee  
## (Keurig K- Classic Coffee Maker (Model K40)

### Functionality: (User makes a cup of coffee)

**User:**
- Turns coffee maker on
- Activates Auto Off
- aits for coffee maker to warm up
- Ensures enough water is in the water reservoir
- Opens pod receptacle
- Selects a cup
- Places cup under pod receptacle
- Selects a pod
- Inserts pod intro receptacle
- Closes pod receptacle
- Presses coffee size button that corresponds to selected cup
- Waits for coffee to fill cup
- Opens pod receptacle
- Removes pod
- Closes pod receptacle
- Removes cup
- Coffee maker shuts off automatically if auto off button was pressed  

**Objects/ Data Structures**

-Coffee Maker (Keurig K-Classic Coffee Maker *Model K40*)
1. Water Resevoir
    - Refill tank indicator: on/off (boolean)  

2. Pod Receptacle
    - Open/Closed (boolean)
    - Pod-in/Pod-out (boolean)  

3. Control Panel
    - Power: on/off (boolean)
    - Auto off: on/off (boolean)
    - Cup size selectors (let)(array)(if else)
        - small
        - medium
        - large  

4. Coffee cup (let)(array)(if else)
    - small
    - medium
    - large  

5. Coffee pod (const)
    - 1 size
    - 1 flavor  

6. Power Supply
    - on/off (boolean)



START  
//BEGIN PROGRAM

    DETERMINE
        IF coffee maker is off 
            THEN turn coffee maker on
        ENDIF
    
    INPUT activate auto off
    
    DETERMINE
        IF water resevoir needs water
            THEN add water
        ENDIF

    DETERMINE
        IF coffee maker is on
            AND water resevoir doesn't need water
            THEN INPUT select cup size
        ENDIF
    
    INPUT select cup size

    INPUT place cup under pod receptacle

    INPUT select pod

    DETERMINE
        IF pod receptacle is open
            THEN insert pod and close pod receptacle
        ELSE
            open pod receptacle
        ENDIF

        CASE selected cup size
            small: INPUT fill small cup
            medium: INPUT fill medium cup
            large: INPUT fill large cup
        ENDCASE

    DETERMINE
        IF cup is filled
            THEN remove pod and trash pod and remove cup
        ENDIF

//END PROGRAM



**Define Objects/ Function**

1. User  
    - pressButton
    - checkResevoir
    - fillResevoir
    - openReceptacle
    - closeReceptacle
    - selectCup
    - placeCup
    - removeCup
    - insertPod
    - removePod  

2. Control Panel
    - powerOff
    - powerOn
    - autoOffOn
    - selectCupSmall
    - selectCupMediun
    - selectCupLarge  