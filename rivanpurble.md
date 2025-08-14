<div align="center">
  <img src="https://github.com/user-attachments/assets/e4d90e60-ee23-4e28-b9c1-ab35e68fed13" alt="Rivan Cyber Training Institute Logo" width="200">
  <h1>RIVAN CYBER TRAINING INSTITUTE</h1>
  <h1>  Purple/Defensive Linux</h1>
</div>

# ⚙️ Network Automation Suite 

[![Ansible](https://img.shields.io/badge/ansible-2.12.0-black?style=for-the-badge&logo=ansible)](https://www.ansible.com/)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](LICENSE)
[![Maintenance](https://img.shields.io/badge/maintained%3F-yes-green?style=for-the-badge)](https://github.com/yourusername/yourrepo/graphs/commit-activity)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen?style=for-the-badge)](CONTRIBUTING.md)

> Enterprise-grade network automation framework for standardized device provisioning and configuration management.

---

## 📂 Repository Structure

- BASIC-CONFIG.yml
- ap.yml  
- call.yml  
- core.yml  
- dns.ps1  
- dns.yml  
- iphone.yml  
- ospfedge.yml  

**Root Files**  
- run_all.yml  
- show.yml  
- README.md  

---

## ⚠️ Critical Configuration Requirements

### Mandatory Pre-Deployment Steps:

1. **File Customization**
   
   Update these configuration files before execution:
   
   - `BASIC-CONFIG.yml`
   - `call.yml`
   - `core.yml`
   - `dns.ps1`
   - `iphone.yml`
   - `ospf.yml`

3. **Monitor Identification**
   
   Replace all underscore placeholders `_` with your actual monitor number:
   
   ```yaml
   # Example:
   monitor_number: 11  # Change the _ to 11 
---
