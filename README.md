
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Dialogo : MonoBehaviour
{
    public GameObject P1;
    public GameObject P2;
    public GameObject P3;
    public GameObject P4;
    public GameObject P5;
    public GameObject P6;
    public GameObject P7;
    public GameObject P8;
    public GameObject Audio;
    public GameObject panel_talk;
    public int count = 0;
    private void OnTriggerStay(Collider other)
    {
        panel_talk.SetActive(true);
    }
    private void OnTriggerExit(Collider other)
    {
        panel_talk.SetActive(false);
        P1.SetActive(false);
        P2.SetActive(false);
        P3.SetActive(false);
        count = 0;
    }
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.E) && count == 0 || count == 1)
        {
            robot_Audio.SetActive(false);
            robot_Audio.SetActive(true);
            P1.SetActive(true);
            P2.SetActive(false);
            ++count;
        }
        p2();
        p3();
        p4();
        p5();
        p6();
        p7();
        p8();
    }
    void p2()
    {
        if (Input.GetMouseButtonDown(1) && count == 2 || count == 3)
        {
            robot_Audio.SetActive(false);
            P1.SetActive(false);
            robot_Audio.SetActive(true);
            P2.SetActive(true);
            ++count;
        }
    }
    void p3()
    {
        if (Input.GetMouseButtonDown(1) && count == 4 || count == 5)
        {
            robot_Audio.SetActive(false);
            P2.SetActive(false);
            robot_Audio.SetActive(true);
            P3.SetActive(true);
            ++count;
        }
    }
    void p4()
    {
        if (Input.GetMouseButtonDown(1) && count == 6 || count == 7)
        {
            robot_Audio.SetActive(false);
            P3.SetActive(false);
            robot_Audio.SetActive(true);
            P4.SetActive(true);
            ++count;
        }
    }
    void p5()
    {
        if (Input.GetMouseButtonDown(1) && count == 8 || count == 9)
        {
            robot_Audio.SetActive(false);
            P4.SetActive(false);
            robot_Audio.SetActive(true);
            ++count;
        }
    }
    void p6()
    {
        if (Input.GetMouseButtonDown(1) && count == 10 || count == 11)
        {
            robot_Audio.SetActive(false);
            P4.SetActive(false);
            robot_Audio.SetActive(true);
            ++count;
        }
    }
    void p7()
    {
        if (Input.GetMouseButtonDown(1) && count == 12 || count == 13)
        {
            robot_Audio.SetActive(false);
            P4.SetActive(false);
            robot_Audio.SetActive(true);
            ++count;
        }
    }
    void p8()
    {
        if (Input.GetMouseButtonDown(1) && count == 14 || count == 15)
        {
            robot_Audio.SetActive(false);
            P4.SetActive(false);
            robot_Audio.SetActive(true);
            count = 0;
        }
    }
}
