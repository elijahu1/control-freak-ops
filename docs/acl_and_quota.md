# Access Control & Quota Configuration

## ACL Commands
```bash
# Public directory (read-only for all)
sudo setfacl -Rm g:admin:r-x,g:editor:r-x,g:viewer:r-x,o:r-x /projects/public
sudo setfacl -Rdm g:admin:r-x,g:editor:r-x,g:viewer:r-x,o:r-x /projects/public

# Team directory (editor RW, viewer RO)
sudo setfacl -Rm g:editor:rwx,g:viewer:r-x,o:--- /projects/team
sudo setfacl -Rdm g:editor:rwx,g:viewer:r-x,o:--- /projects/team

# Confidential directory (admin only)
sudo setfacl -Rm g:admin:rwx,o:--- /projects/confidential
sudo setfacl -Rdm g:admin:rwx,o:--- /projects/confidential

## Quota Setup
```bash
# Initialize quota system
sudo quotacheck -ugm /projects
sudo quotaon -ug /projects

# Set group quotas
sudo setquota -g admin 2000M 2100M 0 0 /projects
sudo setquota -g editor 1000M 1100M 0 0 /projects
sudo setquota -g viewer 200M 250M 0 0 /projects
