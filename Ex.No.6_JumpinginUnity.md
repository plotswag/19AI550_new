# Ex.No: 6  Implementation of Jumping  behaviour- Unity
### DATE:                                                                        
### REGISTER NUMBER :212222243002
### AIM: 
To write a program to simulate the process of jumping in Unity.
### Algorithm:
```
1. Create a new 3D Unity project
2. Add a Plane
3. Right-click Hierarchy → 3D Object → Plane → Rename to Ground
4. Add a Cube (Player)
5. Right-click Hierarchy → 3D Object → Cube → Rename to Player
6. Set Position: (0, 0.5, 0)
7. Add a Rigidbody to the Player
8. With the Player selected: Inspector → Add Component → Rigidbody
9. Set Constraints > Freeze Rotation X, Z (optional for stability)
10.Create the Jump Script and Apply the Script Player
11.Run the game
Press Play
Press Spacebar to jump
Your cube should only jump when touching the ground
```
###
**Program **
```
using UnityEngine;

public class PlayerJump : MonoBehaviour
{
    private Rigidbody rb;
    public float jumpForce = 5f;

    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);

        }
    }


}
```
### Output:

<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/9d4898a5-5c27-4ea9-bceb-5817e75f2ebb" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/09b9f383-c7b6-4755-8feb-dda48e17b4aa" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b87aca7f-f9cc-498b-8470-db7c5179aa54" />




### Result:
Thus the simple jumping behavior was implemented successfully.
