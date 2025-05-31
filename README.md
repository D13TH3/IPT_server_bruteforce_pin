Brute force pin Challenge python with socket library solution process:
How i found the address and the port?
First i download the server file and run it to my computer localy,i open the cmd and then i type the command "netstat -an | findstr LISTENING" it show all network available in my computer i try all posibble ip address and port combination.finally when i try "127.0.0.1:8888" address it open the actvity.

How I Determined What to Send?
Using browser developer tools (Network tab), I saw the form sends a POST request to /verify.
The request body contains a field called (magicNumber).
Constraints Encountered
The server enforces a slowdown after repeated requests.
To avoid being blocked, I added a 1-second sleep() between each attempt.

What I Learned?
How raw HTTP POST requests work at the socket level.
How web servers expect properly formatted HTTP requests.
How simple brute-force attacks can be effective if no security measures are implemented.

Security Improvements I Recommend:
Implement account lockout after several failed attempts.
Add CAPTCHA verification.
Increase PIN length (ex: 6+ digits or use alphanumeric passwords).
Increase the delay before they can input again
Use HTTPS instead of only HTTP.
