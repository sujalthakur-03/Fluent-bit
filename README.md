# Fluent-bit
Fluent Bit is an open-source and high-performance log processor and forwarder designed for collecting, filtering, and forwarding logs and metrics from various sources to multiple destinations. It is widely used in cloud-native environments, containerized applications, and log management pipelines.


## Step-1: Add Server GPG Key 
- The fist step is to add the server GPG key to your keyring to ensure you can get the correct signed packages.
   ```bash
   curl https://packages.fluentbit.io/fluentbit.key | gpg --dearmor > /usr/share/keyrings/fluentbit-keyring.gpg
   ```
## Step-2: Update your sources list
- For Debian, you must add the Fluent Bit APT server entry to your sources lists. Add the following content at bottom of your /etc/apt/sources.list file.
   ```bash
   deb [signed-by=/usr/share/keyrings/fluentbit-keyring.gpg] https://packages.fluentbit.io/debian/${CODENAME} ${CODENAME} main
   ```
## Step-3: Update your repositories database
- Update your system's apt database.
   ```bash
   sudo apt update
   ```
## Step-4: Install Fluent-Bit
- Use the following apt command to install the latest Fluent Bit
   ```bash
   sudo apt install fluent-bit
   ```


## Configuration for ingesting logs from wazuh to graylog
 - Note: To achieve this goal install fluent-bit on wazuh server
 - goto /etc/fluent-bit/
 - Copy the [fluent-bit.conf](https://github.com/Sujal242003/Fluent-bit/blob/main/fluent-bit.conf) and place it in /etc/fluent-bit directory in the wazuh server
