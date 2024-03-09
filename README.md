# Exp02-RollABall
# Aim :
To develop a 3D application for RollABall in unity.

# Algorithm :
# Step1 :
Create a new project.

# Step 2 :
Click Heirarchy -> 3D object -> Select the plane -> 3DObject -> Sphere.

# Step 3 :
Define the physics properties of the surface (Rigidbody).

# Step 4 :
Assets -> Create -> # Script

# Step 5 :
Create a folder name Coding and create a C# file to add the coding in it.

# Step 6 :
To add our C# Script file to our selected object, click on the C# Script file and drag it to our selected objects in the Hierarchy window nad run the application.

# Step 7 :
Run the game and you can move the ball by using the respective keys

# Program :
```
DEVELOPED BY : VAISHNAVI S
REG NO : 212222230165
```
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Rolling : MonoBehaviour
{
    // Start is called before the first frame update
    public float xforce = 5.0f, yforce = 200.0f, zforce = 5.0f;
    void Start()
    {

    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if (Input.GetKey(KeyCode.A))
        {
            x = x - xforce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + xforce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z + zforce;
        }
        if (Input.GetKey(KeyCode.S))
        {
            z = z - zforce;
        }
        if (Input.GetKeyDown(KeyCode.Space))
        {
            y = yforce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);

    }
}
```

## To Reset :
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
public class reset : MonoBehaviour
{
    public float threshold = -50f;
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        if(transform.position.y<threshold)
        {
            SceneManager.LoadScene(SceneManager.GetActiveScene().buildIndex);
        }
    }
}
```
# Output :
![Screenshot 2024-03-07 120257](https://github.com/Vaishnavi-saravanan/Exp02-RollABall/assets/118541897/539fa5f5-c380-40b1-a7e2-411a39193c54)


# Result :
Thus a 3D application for RollABall objects in unity is developed successfully.
