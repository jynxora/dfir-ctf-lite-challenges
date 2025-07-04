# 🧩 CTF-Lite Challenge: July 3 — File Permissions & Suspicious Files


Welcome to a lightweight DFIR-style CTF.  
This scenario helps you sharpen your command-line investigation, file permission analysis, and Linux-based forensic thinking.
It's absolutely beginner firendly and helps build investigative accumen rather than fancy tools that you use thrice a decade.
KICK IN!!!



📁 Setup Instructions (Run this block to auto-create the scenario):

mkdir -p ~/CTF-Lite/staging
cd ~/CTF-Lite/staging
touch README.md notes.txt
echo "Nothing suspicious here." > notes.txt
mkdir secrets
echo "This is a decoy file." > secrets/.invisible.txt
mkdir -p vault/.ssh
echo "Private Key" > vault/.ssh/id_rsa
chmod 600 vault/.ssh/id_rsa
touch vault/passwd_shadow
chmod 000 vault/passwd_shadow
sudo touch vault/root_exploit.sh
sudo chmod 4755 vault/root_exploit.sh
touch /tmp/public.log
chmod 777 /tmp/public.log



🔍 Your Tasks (Write each answer in Notion or anywhere you prefer):


TASK - 1: List all files (including hidden ones) recursively inside ~/CTF-Lite
→ Show command + output

TASK - 2: Find files with world-writable permissions (777 or similar)
→ What risk does this pose?

TASK - 3: Find all files with SUID bit set (Permissions like -rwsr-xr-x)
→ Why is that dangerous?

TASK - 4: Find all files not owned by you (check owner)
→ What command did you use?

TASK - 5: Find any files with no permissions at all (----------)
→ Which file is that? Can you access it? Try it.

TASK - 6: Try reading the fake private key
→ What does the permission 600 mean here? Can you read it?

TASK - 7: Search for all .txt or .log files with find
→ Search only inside ~/CTF-Lite

✅ How to Report/Document:
-------
📁 CTF-Lite — File Permission Challenge


🧱 Task 1: Recursive listing
Command: `...`

Finding: Found hidden file `...` in `...`

🎯 Summary:
- 1 world-writable file (`...`) → potential abuse
- 1 SUID file: `...` — escalation risk
- 1 no-permission file: `...` — inaccessible
  
💬 Takeaways:
- ...
- ...

🧠 You're learning how to:
Detect those quickly,
Interpret their impact,
Defend or attack based on context.
