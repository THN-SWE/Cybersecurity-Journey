#### Why Do the 3 Streams Exist?
- STDIN , STDOUT, STDERR everything is fine but why they created them ? purpose ? 

#### Quick History 
Back in early Unix (1970s), computers were not personal machines. They were:
- Shared
- Accessed via terminals
- Used for automation
- Scripted heavily
The designers wanted programs to be:

> Small, simple, chainable building blocks.

For that to work, programs needed a **standard way to communicate**.

> So they were just wanted to create a standard way to make a computer to take input, output no matter where it recieve input from or give output to. 
> Like writing a function and passing just the argument (input/output)... just for understanding sake 



---

# 🔹 1️⃣ Standard Input (stdin)

This exists because programs need a predictable way to receive data.

Instead of hardcoding:

- “Read from keyboard”
- “Read from file”
- “Read from network”

The program just says:

> “**I read from stdin**.”

Where stdin comes from doesn’t matter.
Keyboard?  
File?  
Another program?
**Doesn’t care.**
**That flexibility is powerful.**

---

# 🔹 2️⃣ Standard Output (stdout)

Programs also need a consistent way to produce results.

Instead of:

- Always printing to screen    
- Or always writing to a file
**They just write to stdout.**

The shell decides where that goes.

Screen?  
File?  
Another program?
That’s the shell’s job.

# 3️⃣ Standard Error (stderr) — The Smart Design Choice

> I can ask why stderr ? it could have used the stdout to show error messages ? 

- Imagine this command:
>  `grep root passwd > result.txt`

- If this command is a valid, it'll write the stdout to result.txt
- If this is invalid, the error message will get written into result.txt
- By separating:
- stdout → normal data
- stderr → problems
- we can prevent it. cool. 

# 🧩 The Big Philosophy

Unix follows this idea:

> **“Do one thing well.”**

**Programs don’t decide where input comes from.**  
**They don’t decide where output goes.**

- Read stdin    
- Write stdout
- Report errors to stderr

**The shell wires everything together.**