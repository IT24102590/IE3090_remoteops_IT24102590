"Compare thread-per-client, fork-per-client and select/poll for a TCP server in C. Give the pros and cons of each, and say which suits a project that needs five simultaneous clients."

"I must implement a fixed line-based text protocol over TCP in C, with AUTH, SYSINFO, LISTPROC, EXEC, PUT, GET, MONITOR START/STOP and QUIT. Don't write the code. Help me plan the program: which functions and modules I need, what state each client session should hold, and what order to build and test each command. Point out any gaps or risks in my plan, and ask me questions before suggesting changes."

 "Show me how to derive a port, session ID and auth token from a registration number like [IT00000000], and give me a few test values so I can check my own calculations are correct."

Core socket implementation

"I'm reading lines from a TCP socket in C. Explain why one recv() call can return a partial line or several lines together, and why this matters for framing. Then review my recv_line() function below and tell me what bugs or edge cases it misses. Explain each problem in plain language rather than just handing me corrected code."

"Explain how to transfer exactly N bytes of a file over TCP using loops around send() and recv(). What happens if the connection drops partway through, and how should my code handle it?"

"I'm writing a C server where each client runs in its own pthread. Explain how I should manage per-client state, close sockets and free memory when a client disconnects, and limit the server to five concurrent sessions with a semaphore. List the common mistakes, such as race conditions, leaks and use-after-free, and show me how to check for each in my own code."

Security and robustness

"Review my EXEC handler below. Is there any way a client could run a command outside the whitelist or inject shell input? Explain each risk you find and why it matters."

"My server lets clients upload and download files by name into a storage directory. List the ways a malicious filename or file size could cause harm, such as path traversal, oversized uploads or half-finished transfers. For each risk, explain how to detect it in C and what error response my protocol should return. Then suggest test cases I can run to prove each protection works."

Debugging and testing

"My client hangs after sending PUT. Here is the relevant code and what I see in the terminal. Don't just fix it. Ask me questions and explain how I can diagnose it myself with tools like strace or ss."

"Here is my protocol specification and my current test table. Suggest additional test cases I may have missed for each mandatory feature, including edge cases such as partial lines, two commands in one packet, an ungraceful disconnect, a rejected PUT, and a sixth simultaneous client. For each, give me the steps, the expected result, and a tool I can use to check it, such as nc, netcat, md5sum or tcpdump."

Report and reflection

"Here are my bullet points about how my concurrency model works. Rewrite them as a concise, formal paragraph. Don't add any claims that aren't in my notes, and tell me if anything looks inconsistent."

"Here is the brief's requirement list and my draft Implementation Report. Check my report against each requirement and tell me what is missing, unclear or inconsistent, such as figure numbers, cross-references, assumptions or screenshot coverage. Don't rewrite my content. Give me a list of problems, so that everything I submit remains my own work and I can explain it in the Viva."
