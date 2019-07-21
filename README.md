# EBV2_proposal
Etherblade.net Ver2” - proposal for “fragmentation support”

Another feature is a “fragmentation support” which is being developed in “Etherblade.net – Ver2” project.

For some telecom operators fragmentation support is not required as they own fibre links and their equipment can natively 
support jumbo frames. In this case transit of original ethernet frame of maximum size of 1500bytes with additional L3 header
is not a problem.
On the contrary small ISPs often use internet for overlay transport which imposes strict MTU limitations. 
So the pseudowire solution they choose must cope with fragmentation issues either via workarounds 
such as “TCPMSS clamping” or by having fragmentation assembly algorithms implemented in the software which are 
CPU intensive and slow. “Etherblade.net Ver2” proposes original method of assembling frame’s fragments at line 
rate speed totally within the datapath with zero CPU/Software involvement.

Please watch the video demonstrating this principle here:
[![EtherBlade.net V2 assembler block conceptual model demonstration](https://img.youtube.com/vi/yz3BlAmwClE/0.jpg)](https://www.youtube.com/watch?v=yz3BlAmwClE "EtherBlade.net V2 assembler block conceptual model demonstration.")
