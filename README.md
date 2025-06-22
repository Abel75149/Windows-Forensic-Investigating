# Windows Forensic Investigation Project

## 📌 Business Case
After a suspected security incident, it's critical to perform a forensic investigation on affected Windows systems to determine the scope, method, and impact of the compromise. This project outlines a structured approach to collecting, analyzing, and reporting digital evidence from Windows environments.

---

## 🎯 Project Objectives
- Identify indicators of compromise (IOCs) and attacker behavior
- Preserve and analyze volatile and non-volatile data
- Reconstruct the timeline of malicious activity
- Support incident response, legal, and compliance requirements

---

## 🧾 Licensing & Tooling Requirements

| Tool / Platform             | Purpose                                | Licensing Notes                          |
|----------------------------|----------------------------------------|------------------------------------------|
| FTK Imager / Autopsy       | Disk imaging and analysis              | Free / Open-source                       |
| Velociraptor / KAPE        | Artifact collection and triage         | Free / Community-supported               |
| Sysinternals Suite         | Live system analysis                   | Free from Microsoft                      |
| Magnet AXIOM / EnCase      | Advanced forensic analysis             | Commercial licenses required             |
| Windows Event Viewer       | Log analysis                           | Built-in                                 |
| ELK Stack / Splunk         | Log aggregation and visualization      | Free tier / Commercial                   |

---

## 🛠️ Investigation Workflow

1. **Initiate Investigation**
   - Define scope and objectives
   - Identify affected systems and stakeholders
   - Preserve chain of custody documentation

2. **Evidence Preservation**
   - Acquire disk images using FTK Imager or dd
   - Capture memory dumps (e.g., with DumpIt or WinPMEM)
   - Collect volatile data (network connections, processes, etc.)

3. **Initial Triage**
   - Use tools like KAPE or Velociraptor to collect key artifacts:
     - Event logs
     - Registry hives
     - Prefetch files
     - LNK files
     - Browser history
     - Scheduled tasks

4. **Timeline Reconstruction**
   - Correlate file system timestamps, logs, and user activity
   - Build a timeline of events using tools like Plaso or Timesketch

5. **IOC & Malware Analysis**
   - Identify suspicious executables, scripts, or persistence mechanisms
   - Analyze malware samples in a sandbox or using static tools (e.g., PEStudio)

6. **Log Analysis**
   - Review Security, System, and Application logs
   - Look for failed logins, privilege escalation, service creation, etc.

7. **User Activity Review**
   - Examine browser history, downloads, and USB usage
   - Review RDP connections and lateral movement indicators

8. **Reporting**
   - Document findings, timelines, and artifacts
   - Provide recommendations for remediation and hardening
   - Maintain evidence integrity for legal or compliance use

9. **Post-Incident Review**
   - Conduct lessons learned session
   - Update incident response playbooks
   - Share IOCs with threat intel platforms

---

## ✅ Best Practices

- Always work on forensic copies, not live systems
- Use write blockers when imaging physical drives
- Maintain detailed logs of every action taken
- Validate tools and hash all collected evidence
- Use multiple tools to cross-verify findings
- Encrypt and securely store all evidence
- Red team your own investigation process periodically

---

## 📋 Project Management Tips

- Assign a lead forensic analyst and legal liaison
- Track investigation progress using a case management system
- Align with NIST 800-86 or ISO/IEC 27037 guidelines
- Schedule regular training and tabletop exercises
- Maintain a forensic readiness policy

---

## 📎 Tools & Technologies

- FTK Imager / Autopsy / Magnet AXIOM
- Velociraptor / KAPE / Plaso
- Sysinternals Suite (Autoruns, Process Explorer, etc.)
- Windows Event Viewer / PowerShell
- Timesketch / ELK Stack / Splunk
