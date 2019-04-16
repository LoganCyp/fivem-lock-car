# FiveM Car Locking Script

### Usage Instructions

- To save the vehicle simply do `/save`
- To lock / unlock the door press the key `H`

### Installation Instructions 

- Fork/download this repository
- Drag the script into your resource folder
- Edit `server.cfg` and add `start Vehicle Control`

### Code Explanation

Change the keys pressed by going to FiveM Controls and change the hex value of the key.Ch

```python

Citizen.CreateThread(function()
    local h_key = 74
    local x_key = 73
    while true do
        Citizen.Wait(1)
        if IsControlJustReleased(1,  h_key --[[ H key ]]) then
            TriggerEvent('lock')
            alert("~b~Vehicle locked/unlocked with ~INPUT_VEH_HEADLIGHT~")
        end
        if IsControlJustReleased(1,  x_key --[[ X key ]]) then
            TriggerEvent('save')
            alert("~b~Vehicle Saved with ~INPUT_VEH_DUCK~")
        end
    end
end)

```
### Coming Soon

- Optional Whitelist for Locking Cars
