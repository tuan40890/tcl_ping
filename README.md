# tcl_ping_script1:
- exec "ping $VAR": This part executes the ping command as an external system command. It's equivalent to typing ping 192.168.0.2 directly into your operating system's command prompt (e.g., Bash on Linux/macOS, Command Prompt on Windows). The exec command captures the standard output of the external ping process.
- puts [...]: This command then prints the captured output from the exec command to the Tcl script's standard output (usually your console).

# tcl_ping_script2:
- ping $address: This assumes that ping is a Tcl procedure or command that has been defined elsewhere in your Tcl script or loaded from a Tcl package. It does not directly execute the system's ping utility.

### Output is the same for either script:
```
Router-IOSXE(tcl)#foreach address {
+>192.168.0.1
+>192.168.0.2
+>192.168.0.3
+>} { ping $address}
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.1, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/1 ms
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.2, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/1 ms
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.0.3, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/1 ms
```
