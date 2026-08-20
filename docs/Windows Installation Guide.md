Vyoma Digital

License Management Windows Client Installation Manual

| Vyoma Digital | 4/22/25 |     |
| ------------- | ------- | --- |

SLM Proxy Installation & Configuration Guide

This document provides clear step-by-step instructions to install, configure, and run the LMS Proxy application on **Windows**. This proxy enables transparent redirection of HTTP(S) traffic for LMS license validation and request forwarding.

**WINDOWS SETUP GUIDE**

**1\. Install .NET Runtime (if not already installed)**

- Download and install the .NET 6 or .NET 8 Runtime from: <https://dotnet.microsoft.com/en-us/download/dotnet>

**2\. Place Executables**

Unzip the FIles to your desired directory, e.g., C:\\LMSProxy

**3\. Configure Routing with netsh**

Use this batch file (setup-port-forwarding.cmd in cmd folder) to redirect HTTP and HTTPS to LMSProxy.

Run as **Administrator**:

setup-port-forwarding.cmd

**5\. Run LMS Proxy in Background**

Create a shortcut to LMSProxy.exe and move it to the Startup folder or use nssm to register it as a service.

**Verification**

After setup:

- From a browser or curl, hit any product URL (e.g., <http://yourdomain.com/yourproduct>) and verify that the LMS Proxy intercepts it.
- Check logs for validation and forwarding steps.

For questions or automation scripting help, email us or go to Support page on our website.
