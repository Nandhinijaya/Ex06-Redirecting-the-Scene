# Ex06-Redirecting-the-Scene
## Aim :
To Redirecting the scene in the unity engine.

## Algorithm :
### Step 1:
 To open the unity engine.

### Step 2: 
Create a new 3D project.

### Step 3:
 Create plane and name it as ground and create cube and name it as player.

### Step 4:
 Add WinText in Hierarchy.

### Step 5:
 Create a C# Script and name it as playercontroller and add the script to player.

### Step 6:
Inside the "CubePlayer" script, import necessary Unity libraries. (i.e.,using UnityEngine; and using UnityEngine.SceneManagement;) 

### Step 7:
Use the R button to change the level2

### Step 8:
Use 'SceneManager.LoadScene() method in the script to handle scene redirection.

### Step 9:
Attach the "SceneRedirector" script to an empty GameObject in your scene.

### Step 10:
Press the specified key (in this case, "R") to test redirection to the "Level2" scene.

### Step 11:
Print the Output and end the program.


## Program :

```C#
DEVELOPED BY: Nandhini E
REGISTER NUMBER : 212222100030
```

## CUBE PLAYER :

```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class CubePlayer : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
        
    }

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }
        
    }
    private void OnCollisionEnter(Collision other)
    {
        if(other.gameObject.tag=="sphere")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}

```
## Output :
![image](https://github.com/user-attachments/assets/3ad44d28-cc56-4be9-a3bf-4bbbae60cb8e)

![image](https://github.com/user-attachments/assets/2b3c0af2-5d72-4d44-baf6-4ae8da848bbe)


## Result :
The above C# coding is successfully redirecting the scene in the unity engine.
