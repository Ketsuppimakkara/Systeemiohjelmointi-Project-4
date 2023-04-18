# Operating systems and system programming course work - Kernel hacking

This is an implementation of a custom system call in Xv6, a light Unix-like operating system for teaching purposes.

Usage:
1. Download and extract the xv6-public-master folder. 
2. Make sure you have qemu installed. I used the command:
      “sudo apt install -y qemu qemu-kvm libvirt-daemon libvirt-clients bridge-utils virt-manager”
3. Open a new shell in the extracted folder.
4. Build and run xv6 with command “make qemu” in the shell
5. Qemu should now be running, you can run the test program in either Qemu or the shell you 
built it from.
6. Run the test program with the command “getreadcount” to display how many times the 
read-systemcall has been called.
  a. The test program can also take one argument. Try using “getreadcount 0” to reset 
    the counter without changing the tracked system call.
  b. You can also give an integer between 1-22 to change which system call is tracked. 
    Changing the tracked system call naturally also resets the counter. The number 
    represents the integer id of the tracked system call. Tracking system call number 22 
    tracks how many times you’ve called the getreadcount system call. By default, the 
    tracked system call is 5 (sys_read)
  c. Try different commands in xv6, such as “ls”, and then use command “getreadcount”
    to see how many times these a specific system call has been called.

Read more about Xv6 here: https://pdos.csail.mit.edu/6.828/2022/xv6.html
