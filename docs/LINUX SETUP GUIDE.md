Vyoma Digital

Linux SLM Client Installation Guide

| Vyoma Digital | 4/22/25 |     |
| ------------- | ------- | --- |

**🐧 LINUX SETUP GUIDE**

**1\. Install .NET Runtime (if not already)**

sudo apt update

sudo apt install -y dotnet-runtime-8.0

**2.** Unzip the files to /opt/lmsproxy or your desired directory

**3\. Move to Deployment Directory**

cd /opt/lmsproxy/cmd

**4\. Configure IP Routing using iptables**

Run:

chmod +x setup-port-forwarding.sh

sudo ./ setup-port-forwarding.sh

**5\. Run LMS Proxy in Background**

nohup sudo ./LMSProxy > /var/log/lmsproxy.log 2>&1 &

Or set it up as a systemd service (ask if needed).

**Verification**

After setup:

- From a browser or curl, hit any product URL (e.g., <http://yourdomain.com/yourproduct>) and verify that the LMS Proxy intercepts it.
- Check logs for validation and forwarding steps.

For questions or automation scripting help, email us or go to Support page on our website.
