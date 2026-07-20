<h1 align="center">Git Looter</h1>

**Git Looter** is a tool designed for penetration testers and security researchers to **dump and reconstruct an entire Git repository** from a publicly exposed `.git` folder on a web server.


<br>


## Security Warning (RCE Risk)
>[!CAUTION]
>
> Malicious Git repositories can contain **hooks** (`.git/hooks/*`) and dangerous configuration directives (such as `core.sshCommand`, `core.editor`, or `core.pager`) that may execute arbitrary commands on your system when you interact with the repository (e.g., during `git checkout`).
>
> **Git Looter** attempts to mitigate this risk by automatically sanitizing `.git/config` before running `git checkout`. However, **no mitigation is completely foolproof**. Always run this tool in **isolated environments** (containers, VMs, or sandboxes) and **never** blindly trust repositories from unknown or untrusted sources.


<br>


## Disclaimer
> [!CAUTION] 
>
> **Use this software at your own risk!**
>
> **YOU AGREE TO:**
> 1. Use only with **proper authorization**
> 2. Comply with **all applicable laws**
> 3. Assume **full liability** for misuse
> 
> **The Developer assume NO liability.**


<br>


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
