what's a netcat
## 6. What's a net cat?

I found this challenge through the hints of another challenge ("nice netcat.."). This one was pretty easy. A quick Google search reveals that netcat (or `nc`) is a network utility used to read from or write to connections using TCP or UDP protocols. There are a few commands for using netcat in Linux.

All I did was copy and paste the URL from the challenge window, adding `nc`, which is what you need to start with when using netcat. By default, netcat assumes you want to perform a port scan unless you specify otherwise. After the URL, I included the port number provided in the challenge description. Running this command gave me the flag.

The command looked something like this:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/ebde0c44-9855-4ab3-8570-a612138f6433">

