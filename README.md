# Tugas-1-Jarkom_Khumaidi-Kharis-Az-zacky_049

# TOPOLOGI
![Topologi](src/topologi.png)

# SUBNETING

**IP Prefix:** `10.89.0.0/22`  
Total Host: **772** host

| Subnet                              | Kebutuhan Host | Netmask |
|------------------------------------|---------------|---------|
| Bidang Guru & Tendik               | 95 host       | /25     | 
| Bidang Kurikulum                   | 220 host      | /24     |
| Bidang Sarana Prasarana            | 45 host       | /26     | 
| Bidang Pengawas Sekolah (Cabang)   | 18 host       | /27     | 
| Server & Admin                      | 6 host        | /28     | 
| Sekretariat                        | 380 host      | /23     | 
| Router                    | 6 host        | /29     | 
| Tunnel                      | 2 host        | /30     | 
| **TOTAL**                           | **772 host**  | **/22** | 

## VLSM
![VLSM](src/vlsm.png)

![Konsep VLSM](src/vlsm_k.png)

## Skema Alokasi VLSM

| Subnet | Kebutuhan Host | Prefix | Available Host | Mask | Network ID (NID) | Broadcast | IP Available (Usable) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **A7 (Sekretariat)** | 380 | /23 | 510 | 255.255.254.0 | **10.89.0.0** | 10.89.1.255 | 10.89.0.1 - 10.89.1.254 |
| **A4 (Bidang Kurikulum)** | 220 | /24 | 254 | 255.255.255.0 | **10.89.2.0** | 10.89.2.255 | 10.89.2.1 - 10.89.2.254 |
| **A3 (Bidang Guru & Tendik)** | 95 | /25 | 126 | 255.255.255.128 | **10.89.3.0** | 10.89.3.127 | 10.89.3.1 - 10.89.3.126 |
| **A5 (Bidang Sarana Prasarana)** | 45 | /26 | 62 | 255.255.255.192 | **10.89.3.128** | 10.89.3.191 | 10.89.3.129 - 10.89.3.190 |
| **A1 (Bidang Pengawas Sekolah)** | 18 | /27 | 30 | 255.255.255.224 | **10.89.3.192** | 10.89.3.223 | 10.89.3.193 - 10.89.3.222 |
| **A6 (Server & Admin)** | 6 | /29 | 6 | 255.255.255.248 | **10.89.3.224** | 10.89.3.231 | 10.89.3.225 - 10.89.3.230 |
| **A8 (Router)** | 6 | /29 | 6 | 255.255.255.248 | **10.89.3.232** | 10.89.3.239 | 10.89.3.233 - 10.89.3.238 |
| **A2 (Tunnel)** | 2 | /30 | 2 | 255.255.255.252 | **10.89.3.240** | 10.89.3.243 | 10.89.3.241 - 10.89.3.242 |
| **TOTAL** | **772** | **/22** | **1022** | **-** | **-** | **-** | **10.89.0.1 - 10.89.3.254** |

## CIDR
![CIDR](src/cidr.png)

![Konsep CIDR](src/cidr_k.png)

## Skema Alokasi CIDR

| Subnet | Kebutuhan Host | Prefix | Available Host | Mask | Network ID (NID) | Broadcast | IP Available (Usable) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **A1 (Bidang Pengawas Sekolah)** | 32 | /27 | 30 | 255.255.255.224 | **10.89.2.0** | 10.89.2.31 | 10.89.2.1 - 10.89.2.30 |
| **A2 (Tunnel)** | 4 | /30 | 2 | 255.255.255.252 | **10.89.2.32** | 10.89.2.35 | 10.89.2.33 - 10.89.2.34 |
| **A3 (Bidang Guru & Tendik)** | 128 | /25 | 126 | 255.255.255.128 | **10.89.3.0** | 10.89.3.127 | 10.89.3.1 - 10.89.3.126 |
| **A4 (Bidang Kurikulum)** | 256 | /24 | 254 | 255.255.255.0 | **10.89.2.0** | 10.89.2.255 | 10.89.2.1 - 10.89.2.254 |
| **A5 (Bidang Sarana Prasarana)** | 64 | /26 | 62 | 255.255.255.192 | **10.89.3.128** | 10.89.3.191 | 10.89.3.129 - 10.89.3.190 |
| **A6 (Server & Admin)** | 8 | /29 | 6 | 255.255.255.248 | **10.89.3.192** | 10.89.3.199 | 10.89.3.193 - 10.89.3.198 |
| **A7 (Sekretariat)** | 512 | /23 | 510 | 255.255.254.0 | **10.89.0.0** | 10.89.1.255 | 10.89.0.1 - 10.89.1.254 |
| **A8 (Router)** | 8 | /29 | 6 | 255.255.255.248 | **10.89.3.200** | 10.89.3.207 | 10.89.3.201 - 10.89.3.206 |
