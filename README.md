# cnt4007---programming-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [CNT4007 – Programming Assignment 2 Solved](https://www.ankitcodinghub.com/product/cnt4007-programming-assignment-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;111050&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CNT4007 - Programming Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
How to submit: Please submit via CANVAS following the guidelines.

Introduction

In this programming assignment, we implement the RDT 3.0, Reliable Data Transfer over a Lossy Channel with bit errors, which is explained in the textbook. In addition, you should be able to design FSMs (finite state machines) for both the sender and receiver sides, based on the description in the textbook for the RDT 3.0.

In this assignment, we will develop and/or modify the sender and receiver of the RDT 3.0 in addition to a Network program, where a network with a lossy channel and bit errors is emulated. Some examples of them are retransmission (sending the same packets), sending correct ACKs. Unless otherwise stated, we use the same assumption and environments as the Programming

Assignment #1. For example, socket is used for TCP/IP communication and the program should be

tested on CISE machines.

Fig. 1

Note: Servers and a Linux computer in the above picture are given as examples and you can access other CISE computers as well, including:

lin114-00, lin114-01, lin114-02, lin114-03, lin114-04, lin114-05, lin114-06, lin114-07, lin114-08, lin114-09, lin114-10, lin114-11.

Problem Outline

This assignment requires three programs running on different machines: a Sender program to send packets to the Network; a Network program to relay the packet from the sender to the receiver; and a Receiver program that receives a packet from the Network. Communications in the opposite direction should also be supported by these programs, i.e., when the Receiver sends back an ACK to the Network, the Network relays it to the Sender so that the Sender can receive the ACK from Receiver.

All three programs should support the RDT 3.0 functions described in the textbook.

Message Format

Before we get into the detail of each program, let’s first take a look at the message format we’re going to use.

Sequence No. ID Checksum Packet Content…

The format is shown above. The first field (1 byte) is the sequence number of the packet, which is either 0 or 1. It’s used for RDT 3.0. The second field (1 byte) is packet ID, which represents the position of the packet in the whole message. It starts from 1. We will see this later. The third field (1 int = 4 bytes) is the checksum of the packet content. To simplify things, here we only add the ANSI value of each character in the content, instead of doing bit operation. And the last field (&gt;= 1 byte) is the actual information in this packet.

Since we will need many packets to test the network and the program, what you should do is to read a message from a given file “message.txt” and break it into many words according to the blank space between them. For example, if the message is:

“You are my sunshine.”

Then there should be 4 packets to contain it. The packets would look like:

0 1 x You

1 2 x are

0 3 x my 1 4 x sunshine.

Here x is a certain checksum number. We assume each message ends with a period ‘.’ so if we find a period at the end of a packet, that means the whole message is complete. The ACK format is simpler. It only has the sequence number field (1 byte), which takes the value 0 or 1, and the checksum value (1 byte). The checksum is initially set to 0 in ACK.

Network Program

In this assignment, the Network program is an emulator of a network. The main function of this program is to relay a packet and acknowledgement between a sender and a receiver. It’s like a bridge between the two ends.

In order to emulate the lossy channel with bit errors, we let the Network choose an operation from the following three options: PASS, CORRUPT or DROP whenever it needs to relay a packet/ACK. In this implementation, the Network picks one of the three operations RANDOMLY with probability 0.5 for PASS, 0.25 for both CORRUPT and DROP. The reason we need to do this is that we want to test if the RDT 3.0 works correctly. Please see the Appendix for hints on generating random values.

If the chosen operation is PASS, the packet is forwarded to the receiver without any change. If CORRUPT, we add 1 to the checksum field. This is simpler than flip some random bits. If the operation is DROP, instead we drop the packet or ACK, which is to be relayed; we send a DROP message to the sender. We can use ACK2 for DROP message, i.e., ACK with sequence number 2.

The reason we need to do this is that we want to emulate a timeout. In a real RDT 3.0 system, if a packet or ACK is dropped, the sender will not receive any reply, so after a certain amount of time, it will timeout and resend the previous packet. However, we want to make thing a bit easier and avoid using timer function and interrupt handling. Thus, an emulated timeout is used here, that is, when the sender receives a DROP message, it will consider it as a timeout.

When the Network gets a packet or ACK, it will print on the screen the packet type, ID (no ID for ACK) and the operation it picks. For example:

Received: Packet0, 5, DROP

Received: ACK1, PASS

Receiver Program

The receiver program utilizes the RDT 3.0 receiver side protocol by returning a proper ACK after receiving a packet. The important thing is that your receiver needs to cooperate with the RDT 3.0 sender and sends back ACK0 or ACK1 to handle PASS or CORRUPT packet.

When a packet arrives, the receiver will perform the checksum and examine the serial number and ID to see if this packet is wanted and not corrupted. Every time the receiver got a packet, the screen should display: its current state, total number of received packets so far (including corrupted), print whole packet, and the proper ACK to be transmitted. For example:

Waiting 0, 10, 1 4 x sunshine., ACK1

Waiting 1, 11, 1 5 x gators, ACK1

If the packet containing the end of the whole message is received, the receiver should also display the message with blanks between each word as the following:

Message: You are my sunshine.

Sender Program

The sender program first reads the message file and converts it into many packets. Then it sends a packet to the Network and awaits a relayed ACK from the RDT 3.0 receiver. It should be able to cooperate with your RDT 3.0 receiver, meaning that it needs to be able to send a new packet or resend the same packet according to different network situations such as PASS, CORRUPT or DROP. This is really determined by the ACK it received or by timeout.

Moreover, when it receives a DROP message from the Network, it realizes that this is the timeout and then resends the same packet. Every time an ACK or DROP is received, the sender should display on screen: its current state, total number of packets sent so far (including failure), packet received, proper action. For Example (Here Packet0 means the serial number 0, not the ID):

Waiting ACK0, 8, DROP, resend Packet0

Waiting ACK0, 15, ACK0, no more packets to send

Waiting ACK1, 120, ACK1, send Packet0

Running the System

The three programs are running at three different CISE machines. The port number can be the same as PA#1. The Network is started first and waits for 2 incoming connections. Network program is implemented with two sockets; one for the sender and the other for the receiver, as shown in Fig. 1.

Then the sender and the receiver are started and both connected to the Network using URL and port number. So that means the Network program might need two threads/processes to handle the two connections simultaneously.

Here is an example on how to run the emulation:

[Java] java network [portNumber]

[Java] java receiver [URL] [portNumber]

[Java] java sender [URL] [portNumber] [MessageFileName]

Important Note

• The URL, port number and file name should be command line input, do NOT hard code it.

• Print the required messages on all 3 machines according to the specified format.

• Test your program on CISE machines; make sure they do work properly.

System Termination

After receiving the final correct ACK from the receiver, the sender will initiate the termination process. It will send a single byte -1 to the Network and exit. Upon receiving -1, the Network will also send -1 to receiver and exit. The receiver exits the last when it got -1 from Network.

Note on Run-away Processes for the Graceful Termination:

Your program should terminate gracefully. While testing your programs, run-away processes might exist. However, these run-away processes should be killed. Please check frequently if there are any remaining processes after termination. CISE department has a policy regarding this issue and your access to the department machines might be restricted if you do not clean these processes properly.

Some useful Linux/Unix commands:

To check your running processes: ps -u &lt;your-username&gt;

To kill a process: kill -9 pid

To kill all Java processes: killall java

To check processes on remote hosts: ssh &lt;host-name&gt; ps -u &lt;your-username&gt; To clean Java: ssh &lt;host-name&gt; killall java

Report

Submitted report file should be named report.pdf or .txt and include the following:

• Your personal information: Full name, UF ID, and Email • How to compile and run your code under which environment.

• Description of your code structure.

• Show some of the execution results.

– Discuss the results you got with your program and include screenshots.

• Explain about the bugs, missing items and limitations if there is any.

– Honesty is valued here.

Submission Guidelines:

1. The source code files should be named “sender.java”,” receiver.java” and “network.java”.

2. Only submit your Java source code files and report, do not include .obj/.class or executable.

3. Include “makefile” if you have one. (optional)

4. Include the report in .pdf or .txt format. Name it “report.pdf/txt”.

5. Zip all your files into a packet: Firstname_Lastname_ID.zip

Grading Criteria:

Correct Implementation / 50%

Graceful Termination / 20%

Report / Code Style 30%

Total: 100%

Appendix: Generating Random Number According to Some Probability

To get a random event with certain probability, we can generate a uniformly distributed random number between (0, 1) and check if the number is within the probability value. For example, if the number we get is less than 0.5, we choose PASS. If it’s between 0.5 and 0.75, we choose CORRUPT and if it’s larger than 0.75, we pick DROP.

The following is an example to show how to generate random values.

import java.util.*; public class RandomJava {

Random r;

RandomJava() { r = new Random(); }

public double getRandomValue() { return r.nextDouble(); }

public static void main(String[] args)

{

RandomJava rj = new RandomJava(); //test random variables

for (int i=0;i&lt;10;i++ ) {

System.out.println(“random:

“+rj.getRandomValue());

}

} }
