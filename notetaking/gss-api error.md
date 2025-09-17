[[SSH]]
1. User Permissions or Sudo Configuration:**
    
    - **Passwordless sudo:** Your script likely assumes that `sudo` commands run without a password prompt. If for some reason the user running the script no longer has passwordless sudo rights, the script will fail.
    - **Sudoers File Change:** A change in the VM’s configuration (or a new base image) might have altered the `/etc/sudoers` file, removing the permission that allowed your user to run sudo commands without a password.
2. **SSH and OS Login Settings:**
    
    - **OS Login Enabled:** Google sometimes updates VM settings. If OS Login was enabled on your dev project (even accidentally), the SSH connection might be using different credentials. OS Login manages user access via IAM roles rather than local accounts, which could cause a mismatch in permissions.
    - **GSSAPI Authentication:** A change in the SSH configuration might be forcing the use of GSSAPI. If the SSH client on the VM or your deployment system has been updated or reconfigured, it may be attempting GSSAPI authentication where it previously did not.
3. **Changes in the PR Deployment Pipeline:**
    
    - **Different User/Context:** Perhaps the PR branch deploys the VM using a slightly different process or user account. For example, if the master branch uses a service account that has full sudo rights, but the PR branch uses a different account, that could explain the discrepancy.
    - **Script Execution Order:** If the script runs too early in the VM startup (before proper SSH keys or user configurations are applied), it might hit permission issues.
i want to install some dependencies in a VM (gcp) in the setup-app.sh file I added some sudo-install statements, this same pr. was deployed for about a month to dev, but for some reason has started failing.. ie it says Permission denied, gssapi.. something.. during the startup. if I redeploy master and try to access the VM, then I do not get the error, but even In master build I am able to perform the sudo install statements without any issue,.. so what could have changed for this permission denied error to happen.

