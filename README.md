## Hi there 👋
I’m a student in FRC interested in systems programming, infrastructure, and robotics software.

I mainly code in Java, Rust, C++, Python and Go.

I’m interested in distributed systems, networking, operating systems, and infrastructure design, with a focus on performance and scalability.

[![Maceo's GitHub stats](https://github-readme-stats.vercel.app/api?username=maceolsweeney)](https://github.com/anuraghazra/github-readme-stats)



if (-not (Get-Service sshd -ErrorAction SilentlyContinue)) { Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0 }
Set-Service sshd -StartupType Automatic
Start-Service sshd
New-NetFirewallRule -Name sshd-direct-cable -DisplayName "OpenSSH Server (direct cable)" -Direction Inbound -Protocol TCP -LocalPort 22 -InterfaceAlias "Ethernet 3" -RemoteAddress 169.254.0.0/16 -Action Allow
