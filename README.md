# RollaBall

## Aim:
To Roll a Ball using C# program in unity.


## Algorithm:

### step1: 
File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (MiniGame)

### step2: 
Heirarchy -> 3D Object-> Plane 
[ Right side-> Inspector-> Change the name of plane (Name: Ground)
Transform -> Reset
Edit -> FrameSelected ]

### Step3: 
Scale the ground by giving the scaling value as x=4 y=1 z=4

### step4:
Heirarchy -> 3D Object-> Sphere
[ Right side-> Inspector-> Change the name of plane (Name: Player)
Transform -> Reset
Edit -> FrameSelected 
Transform -> Position -> y=0.5]

### step5:
Hierarchy -> DirectionalLight
[ Inspector -> Change the color to white (255,255,255)]

### step6:
Create a folder in project and name as Materials
[Material folder -> Create -> Material (Name: Background)
Inspector ->Surface Inputs ->BaseMAp (Choose the color)
Metallic map-> 0
Smoothness -> 0.25
Drag the Background to the plane and release the mouse

Material folder -> Create -> Material (Name: Sphere)
Inspector ->Surface Inputs ->BaseMAp (Choose the color)
Metallic map-> 0
Smoothness -> 0.75
Drag the Sphere material to the ball and release the mouse

### step7:
Hierarchy -> Player-> Inspector ->Add component-> Rigidbody

### step8:
Create a new script -> Create a folder in project (Name: Scripts)
Hierarchy -> Player -> Inspector-> AddComponent-> NewScripts-> PlayerController( Click create and Add)
Copy the PlayerController and drag to Script folder
Double click the PlayerController file and type the coding

## Program:
```
Developed by: K.Jhansi
refno:212221230045

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
namespace Name
{
public class NewBehaviourScript : MonoBehaviour
{
    public float xforce = 10.0f;
    public float yforce = 300.0f;
    public float zforce = 10.0f;
    // Update is called once per frame

    void Update()
    {
       float x = 0.0f;
       float y = 0.0f;
       float z = 0.0f;
       if (Input.GetKey(KeyCode.S))
        {
            x=x-xforce;   
        }
        if(Input.GetKey(KeyCode.O))
        {
            x = x + xforce;   
        }
        if(Input.GetKey(KeyCode.W))
        {
            z = z + zforce;   
        }
        if(Input.GetKey(KeyCode.M))
        {
            z = z - zforce;   
        }
        if(Input.GetKeyDown(KeyCode.Space))
        {
             y = yforce;    
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}
}
```
## Output:
![output](https://github.com/jhansi21005096/RollaBall/blob/main/outputroll.png)

## Result:
Thus a C# program to Roll a Ball in unity is written and executed sucessfully.
