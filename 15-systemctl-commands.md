# Linux `systemctl` Commands

`systemctl` is a command-line utility used to control and manage services on systems using `systemd`.

It can be used to start, stop, restart, enable, disable, and check the status of system services.

---

## 1. Check Service Status

Displays the current status of a service.

```bash
systemctl status service-name

Example:

systemctl status apache2

Purpose:

1.Checks whether a service is running.
2.Displays service state and recent log information.
3.Shows the process ID and service configuration details.



## 2. Start a Service

Starts a stopped service.

sudo systemctl start service-name

Example:

sudo systemctl start apache2


## 3. Stop a Service

Stops a running service.

sudo systemctl stop service-name

Example:

sudo systemctl stop apache2


## 4. Restart a Service

Stops and starts a service again.

sudo systemctl restart service-name

Example:

sudo systemctl restart apache2

Useful after changing a service's configuration.



## 5. Reload a Service

Reloads a service's configuration without completely stopping the service.

sudo systemctl reload service-name

Example:

sudo systemctl reload apache2

Whether reload is supported depends on the service.



## 6. Enable a Service

Configures a service to start automatically when the system boots.

sudo systemctl enable service-name

Example:

sudo systemctl enable apache2


## 7. Disable a Service

Prevents a service from starting automatically at boot.

sudo systemctl disable service-name

Example:

sudo systemctl disable apache2


## 8. Check Whether a Service Is Active
systemctl is-active service-name

Example:

systemctl is-active apache2

Possible output:

active


## 9. Check Whether a Service Is Enabled
systemctl is-enabled service-name

Example:

systemctl is-enabled apache2

Possible output:

enabled


## 10. List Running Services

To list currently active service units:

systemctl list-units --type=service


## 11. List Failed Services

Displays services that have failed:

systemctl --failed


🔄 Basic Service Management Workflow:

A common service-management workflow is:

sudo systemctl start service-name
systemctl status service-name
sudo systemctl restart service-name
sudo systemctl enable service-name.


___________________________________
