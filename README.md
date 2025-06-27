# ElevateLabs-internship-task4

# Task 4: Setup and Use a Firewall on Windows/Linux

## Objective
Configure and test basic firewall rules to allow or block traffic.
---

## Tools Used
- **Windows Defender Firewall** on Windows 11
- **Telnet** to test connectivity

---

## Windows Firewall Configuration

### Step-by-Step
For this task, I decided to block telnet connection.

1. Launch Windows Firewall from `control firewall.cpl`
2. Click **Advanced Settings**
3. Add a new **Inbound Rule**:
- Rule Type: **Port**
- Port: **23**(telnet)
- Protocol: **TCP**
- Action: **Block the connection**
- Profile: All (Domain, Private, Public)
- Name: `Blocked Telnet(or anything you like)`

4. Test with:
```powershell
telnet 127.0.0.1 23
```
Output: `Connect failed` → Rule works

5. **Remove Rule**:
- Open Advanced Settings → Inbound Rules → Delete `Block Telnet Port 23`

---

## Summary – How Firewalls Filter Traffic

A firewall observes and examines network traffic according to rules that are configured. It determines whether traffic is permitted or blocked based on criteria such as port, IP, or protocol. Firewalls can:
- Restrict unauthorized access
- Block unused/insecure ports (i.e., Telnet)
- Permit secure connections (i.e., SSH)

Windows Firewall allows GUI-based control for rule creation and maintenance.

---

## Outcome
- Acquired basic hands-on experience with host-based firewalls
- Learned how to manage incoming traffic
- Gained experience in creating, testing, and deleting rules
