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

**2 Start a packet capture on an ethernet port and save it to a file.**

Open **The Wireshark Network Analyzer** by clicking on it at the bottom of the screen.

Click the drop-down arrow and make sure **🗹 Wired** is selected.

Select **ens5** to run you packet capture and then click on the **blue shark fin** to **start** capturing packets.

After a few moments click on the **red box** to **stop** capturing packets.

**\*\*\*DO NOT keep running a capture, you can run out of memory. \*\*\***

Save the file and call it Step 2. **\*\*\*Some options will be grayed out while the capture is running. \*\*\***

Open the Step 2 file.

Re-Start a capture.

**3 Use a display filter to detect HTTPS packets.**

Practice Task: Start Wireshark capture and detect **HTTP** packets.

Go Mozilla Firefox Browser

Enter **duckduckgo.com** the Browser. Before you start go back to Wireshark.

Wireshark hit the Blue Shark Fin to start a capture, now go back to Mozilla Firefox Browser and load godaddy.com.

In Wireshark **stop the capture**, save it using File name: **Step2**.

Apply display filter **tcp.port==443.** Press on the **Blue Arrow** to **apply the filter.** This displays activity on port 443.

Reload the file and locate the **Client Hello** and note the Destination **52.149.246.39**.

Copy and paste this **IP Address** into you **Mozilla Firefox browser** to launch the **duckduckgo.com** web page

**Capstone Task: Use Wireshark to capture and observe ethernet packets on HTTP and HTTPS ports. 4m**

**4 Visit a webpage and detect its IP address using a display filer.**

Go to Mozilla Firefox Browser, then settings, the Cookies and Site Data to Clear Data.

Go back to Wireshark, clear the filter, close the capture file, and start a capture.

In browser go to Google.com

Go back to Wireshark to stop the capture. Set the display filter to tcp.port==443

Find **Hello Client** and note the Destination IP, which should be Google.com. Confirm via your browser.
