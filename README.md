# Wireshark-for-Beginners







**Wireshark for Beginners: Capture Packets**

The IT manager wants to be able to capture ethernet network web traffic on the server and be able to detect certain IP addresses as well.
To be successful in this project, you will need some basic Linux Command Line Knowledge and some exposure to Computer Networks.
You are working for a company that wants to detect certain TCP/IP network traffic on their server, specifically web traffic. Your task is to set up and demonstrate Wireshark’s packet capture capabilities.

**1 Install and setup Wireshark for non-super users belonging to the Wireshark Group.**

Type **sudo usermod -aG wireshark $USER** in the Command Line and press Enter
**\-a** means to append, while **G** mean Group, so we are adding **Wireshark** to the Group **rhyme**.
This means we are not running **Wireshark** as **sudo** or **super user**, we are running it as **rhyme**.
Wireshark **should not** be run as superuser for **security reasons**.
![Wire 66 1 0](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/6398908d-f828-4664-9077-9fea530fd5b0)

**2 Start a packet capture on an ethernet port and save it to a file.**

Open **The Wireshark Network Analyzer** by clicking on it at the bottom of the screen.

Click the drop-down arrow and make sure **🗹 Wired** is selected. ![Wire 66 2 0](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/17d9dbc1-1d90-43f6-812c-9dabf1dbced6)

Select **ens5** to run you packet capture and then click on the **blue shark fin** to **start** capturing packets.![Wire 66 2 1](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/6f958198-102e-4efc-8076-e686767b6197)

After a few moments click on the **red box** to **stop** capturing packets.

**\*\*\*DO NOT keep running a capture, you can run out of memory. \*\*\***

Save the file and call it Step 2. **\*\*\*Some options will be grayed out while the capture is running. \*\*\*** ![Wire 66 2 2](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/4dd2870b-08f5-4f3a-95bc-fae6db96deb6)

Open the Step 2 file.![Wire 66 2 3](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/0d4907ae-435c-4a3e-aeeb-0281f5b701a3)

Re-Start a capture.![Wire 66 2 4](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/1a1f1f35-5da7-47e3-9a2b-9da4343bd06d)


**3 Use a display filter to detect HTTPS packets.**









![Wire 66 3 3](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/0ed14616-4422-48e2-a555-4686a518a072)

![Wire 66 3 1](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/b1806d68-55f1-423f-8360-a8e89ea9f2d9)


Practice Task: Start Wireshark capture and detect **HTTP** packets.

Go Mozilla Firefox Browser. ![Wire 66 3 0](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/1b9b3488-1e42-41cc-bd09-1847e01bbfd5)

Enter **duckduckgo.com** the Browser. Before you start go back to Wireshark.

Wireshark hit the Blue Shark Fin to start a capture, now go back to Mozilla Firefox Browser and load godaddy.com.![Wire 66 3 2](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/117817ed-74ed-419c-bc5a-7feb96ab8512)

In Wireshark **stop the capture**, save it using File name: **Step2**.![Wire 66 3 4](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/c555cf4e-a094-4fe9-90d6-6480238c8351)
![Wire 66 3 5](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/edab806b-1567-4da0-9c2b-f39ad7a560f0)
Apply display filter **tcp.port==443.** Press on the **Blue Arrow** to **apply the filter.** This displays activity on port 443.
![Wire 66 3 7](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/ee6e4dc5-e948-427f-984a-f3ff1e43674e)

Reload the file and locate the **Client Hello** and note the Destination **52.149.246.39**.![Wire 66 3 8](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/7e2d20a3-89fc-4468-a595-04386bc9affc)

Copy and paste this **IP Address** into you **Mozilla Firefox browser** to launch the **duckduckgo.com** web page. ![Wire 66 3](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/8bb471ad-4fae-46f3-9ccd-686d246acbc4)
![Wire 66 3 9](https://github.com/TDCybersecurity/Wireshark-for-Beginners-/assets/142702123/fa85ffe1-861c-48ff-8e73-9a564700256e)

**Capstone Task: Use Wireshark to capture and observe ethernet packets on HTTP and HTTPS ports. 4m**

**4 Visit a webpage and detect its IP address using a display filer.**

Go to Mozilla Firefox Browser, then settings, the Cookies and Site Data to Clear Data.

Go back to Wireshark, clear the filter, close the capture file, and start a capture.

In browser go to Google.com

Go back to Wireshark to stop the capture. Set the display filter to tcp.port==443

Find **Hello Client** and note the Destination IP, which should be Google.com. Confirm via your browser.
