# 🔒 Control Freak Ops Project (Week 2 – SysAdmin Cohort)

**Mission:** Build a secure multi-user environment with military-grade access control for FinTech Fury Inc.

---

## 💡 Core Components

- 👥 Role-based access control (admin/editor/viewer)
- 📂 Directory permissions blueprint enforced via ACLs
- 🚫 Disk quotas per security group
- 📜 Full audit trail for sensitive operations
- 🔐 Sudo rights containment to admin group

---

## 🛡️ Security Arsenal

- `setfacl`-enforced directory permissions
- `auditd` monitoring on confidential access
- Password policies with `chage` enforcement
- `cron`-powered audit summarization
- Group-level disk quotas
- Least-privilege sudo configurations

---

## 📁 Project Structure

user-data/ → User CSV definitions
scripts/ → Onboarding & verification scripts
docs/ → ACL/quota configuration docs
logs/ → Operation audit trails
projects/ → Permission-controlled directories
screenshots/ → Proof of compliance
setup/ → Quota/audit configuration files


---

## ✅ Verification Checklist

- [ ] Role-based access functional
- [ ] Quotas enforced per group
- [ ] Confidential access logged
- [ ] Viewer can't modify protected files
- [ ] Admin has full sudo privileges
