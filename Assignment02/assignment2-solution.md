TODO: rename to .txt

# Assignment 2
## task2-solution:
- Set up a UDP server using nc
	- find own ip address using ifconfig
	- nc -ulp 53

- Construct UDP datagram
	- send(IP(src="192.168.0.1", dst="10.0.2.15") / UDP(sport=53,dport=53) / Raw(load="hello world!\n"), count=1)
	- IP(...) sets router as source and localhost as destination
	- UDP(...) sets source and destination ports (chosen arbitrarily)
	- Raw(...) specifies payload
	- count specifies number of packages to send
	- send sends the package.
	- one could also construct package declaring variables, i.e. a=IP() / a.src="192.168.0.1" / b=UDP(...) / send(a/b/c)
