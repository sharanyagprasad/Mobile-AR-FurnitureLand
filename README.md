using System.Collections;
using System.Collections.Generic;
using UnityEngine;
 
public class FLController : MonoBehaviour
{
    private bool soundplayed = false;
    // Start is called before the first frame update
 
    // Update is called once per frame
    void Update()
    {
        if (!soundplayed && transform.localPosition.y < 0.05)
        {
            soundplayed = true;
            GetComponent<AudioSource>().Play();
        }
 
    }
    public void Movefurniture()
    {
        transform.localPosition += new Vector3(0, 10, 0);
        soundplayed = false;
 
    }
}
 

