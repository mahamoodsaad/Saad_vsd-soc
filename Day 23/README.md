# Post-Routing STA analysis of VSDBabySoC Design
#### Running STA
To perform post-route Static Timing Analysis (STA) using Docker, follow these steps to execute the sta_across_pvt_route.tcl script. Start by launching a Docker container with your local project directory mounted. Then, run the script inside the container. This process will automatically generate timing reports—including setup and hold slack, Worst Negative Slack (WNS), and Total Negative Slack (TNS)—within the mounted /data directory. Running STA inside Docker ensures a stable, consistent, and reproducible environment for timing verification across different PVT corners.

<img width="1209" height="761" alt="Screenshot 2025-10-03 at 12 12 31 AM" src="https://github.com/user-attachments/assets/699bc594-a136-493b-b2d8-54e5e72aef17" />

<img width="1206" height="771" alt="Screenshot 2025-10-03 at 12 12 40 AM" src="https://github.com/user-attachments/assets/5cfcc469-4cf9-4407-a255-e51872a353c7" />

After executing the STA script, navigate to the `STA_OUTPUT/route/` directory to access all the generated timing reports. This folder contains detailed path delay reports for each library corner (`min_max_*.txt`), along with summary files such as `sta_worst_max_slack.txt` and `sta_worst_min_slack.txt` for the worst setup and hold slacks, respectively. Additionally, `sta_tns.txt` and `sta_wns.txt` provide the Total Negative Slack (TNS) and Worst Negative Slack (WNS) values. Together, these reports offer a comprehensive view of the BabySoC design’s timing behavior after the routing stage.

<img width="1212" height="764" alt="Screenshot 2025-10-03 at 12 14 11 AM" src="https://github.com/user-attachments/assets/722c5f5f-460d-4dca-9687-6954968d0a70" />

## Pre-Layout and Post-routing Results Comparison:
<img width="1112" height="612" alt="Screenshot 2025-10-10 at 12 16 28 PM" src="https://github.com/user-attachments/assets/4e0b19ad-b18e-4a93-87aa-95cfa0dd1576" />
<img width="1091" height="629" alt="Screenshot 2025-10-10 at 12 16 47 PM" src="https://github.com/user-attachments/assets/483d3ab0-e713-4129-9d18-358996d9b35c" />

## Comparison Graphs:
<img width="1314" height="740" alt="Screenshot 2025-10-10 at 4 09 40 PM" src="https://github.com/user-attachments/assets/f6feb60d-0923-4a47-a85a-4b922bd5ff2c" />

<img width="1342" height="760" alt="Screenshot 2025-10-10 at 4 09 57 PM" src="https://github.com/user-attachments/assets/60f5929e-7dab-49e7-97dd-e54ccdc04567" />

<img width="1512" height="822" alt="Screenshot 2025-10-10 at 4 10 25 PM" src="https://github.com/user-attachments/assets/7055feab-903e-46bd-8b20-4f644b52e2be" />

<img width="1437" height="826" alt="Screenshot 2025-10-10 at 4 10 44 PM" src="https://github.com/user-attachments/assets/1e5f50ff-fba7-4b05-b7fc-73b721be1412" />
