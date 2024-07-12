# GI

# NETWORK BASH
-----------------------------------------------------------------
#!/bin/bash

# Define the IP range
network_prefix="192.168.100."
start_range=10
end_range=25

# File to store active IPs
output_file="IPs.txt"

# Clear the output file if it exists
> "$output_file"

# Loop through the range and ping each IP
for i in $(seq $start_range $end_range); do
    ip="${network_prefix}${i}"
    # Ping the IP address twice and check if it is reachable
    if ping -c 2 -W 1 "$ip" > /dev/null 2>&1; then
        echo "$ip is active"
        echo "$ip" >> "$output_file"
    else
        echo "$ip is not active"
    fi
done

echo "Active IPs have been recorded in $output_file."
-------------------------------------------------------------------------

![image](https://github.com/user-attachments/assets/977e666a-ce42-4eb7-8c4e-10bec7933a22)
![image1](https://github.com/user-attachments/assets/1c21b433-aee1-4317-97cd-79dc8b909977)
![image2](https://github.com/user-attachments/assets/14ee6aa6-924a-4bf2-aa15-29a592c24e91)
![script](https://github.com/user-attachments/assets/86247526-4374-494d-b4d9-4758330b3009)
![script1](https://github.com/user-attachments/assets/02032456-7d3b-4e36-8311-b72ab4f33ee1)
![chmod](https://github.com/user-attachments/assets/0414c21b-f6b2-4033-bcb8-bf2603a4cb6e)
![ssh](https://github.com/user-attachments/assets/47da971b-d9a7-4eca-b41f-8c44bc69f497)





