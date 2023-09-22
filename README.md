# Jarkom-Modul-1-I05-2023

## Modul 1 Jarkom 2023 I05 Formal Report

Group Members:
| No |  Name    |  NRP  |
| ---       |   ---     |---  |
|     1     |     Khairiya Maisa Putri    | 5025211192 |
|     2     |     Talitha Hayyinas Sahala    |  5025211263 |

# No. 1
## Question

# No. 2
## Question
> Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

**answer:** ```gunicorn```

**Wireshark:**

<img width="1440" alt="Screenshot 2023-09-18 at 19 57 38" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/e0a0e81b-4e6b-4f23-bb7a-c3b321021be5">

**Terminal:**

<img width="562" alt="Screenshot 2023-09-18 at 19 58 23" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/c9434d8d-94cb-4bf3-91c5-ff6e749eec6d">

## Explanation
To find the web server that the practicum portal used, I filtered the packets using ```http``` on the file that was given. After that, I search for the same IP address as the portal, which is on the no 1765. Then, I double clicked on it and all of the details will come up at the bottom of the screen (the black part on the wireshark screen). And then we can see the the server that is used under the _Hypertext Transfer Protocol,_ which is ```gunicorn```.

# No. 3
## Question
>a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

**answer:** ```21```

**Wireshark:**

**Terminal:**

## Explanation
a. To do this question, we can use a query filter.  We use ip.src or ip.dst for the address and udp.port for the desired port. In this context, we need to apply the filter query (ip.src == 239.255.255.250 or ip.dst == 239.255.255.250) && udp.port == 3702. The result will display all packets that match the filter query. After counting, the total is 21 packets.

## Question
b. Protokol layer transport apa yang digunakan?

**answer:** ```UDP```

**Wireshark:**

**Terminal:**

## Explanation
b. for this question we can see the protocol inside the protocol column, and it shows UDP.

# No. 4
## Question
> Berapa nilai checksum yang didapat dari header pada paket nomor 130?

**answer:** ```0x18e5```

**Wireshark:**

<img width="1440" alt="4" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/0f0c5b11-9c0a-4889-b5f1-01be7f67d4d4">

**Terminal:**

<img width="568" alt="4 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/337d6b14-7da1-473f-b38e-fbbce0c66ebf">

## Explanation
To find the checksum value on the packet no 130, first I opened the file that was given. Then, I searched for the packet no 130 and double clicked it. And we will see the checksum value under the _User Datagram Protocol_, which is ```0x18e5```.

# No. 5
## Question
> a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

**answer:** ```60```
> b. Port berapakah pada server yang digunakan untuk service SMTP?

**answer:** ```25```
> c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

**answer:** ```74.53.140.153```

**Wireshark:**

<img width="1440" alt="5 wireshark" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/50aa625d-1368-4855-aa1b-ce83225737e0">

<img width="1440" alt="5 password" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/43b19c17-e44d-4fd2-9df7-aecc0b41548b">

**To decode the zip password:**

<img width="904" alt="5 decode" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/87a94bf6-7b17-4205-b953-1ea21a54bde0">

**Inside of the zip file:**

<img width="1440" alt="5 file buat instance" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/e7f70bb9-417e-473f-ac68-0df484197124">

**To find the answers for the questions on the terminal:**

<img width="1440" alt="5 answers" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/4bb67f7b-0197-4b1b-9daa-7e4c158a5ec3">

**Terminal:**

<img width="620" alt="5 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/a33574a3-148e-4fb4-a2d3-82c1fa5bdc1d">

## Explanation
For this answer we were given 2 files, which are a  **zip** file, and a **pcap** file. To open the zip file we have to find its password using the pcap file. First I filtered all the packets using ```tcp.stream eq 0``` and then search for the packet that has _pass_ in it. Then I right cliked and choose ```Follow``` then ```TCP Stream```. It will open a new window, and you will find the password which is ```NWltcGxlUGFzNXdvcmQ=```, but you will still need to decode it in order to use it to open the zip file. Since it says that it needs to be decoded from Base64, I used a website where it can decode from Base64. After decoding it, I got the real password that can be used to open the zip file which is ```5implePas5word```. After successfully open the zip file, it will show the **instance** that we can copy and paste to the terminal to get the questions that we need to answer. 

# No. 6
## Question

# No. 7
## Question
> Berapa jumlah packet yang menuju IP 184.87.193.88?

**answer:** ```6```

**Wireshark:**

<img width="1440" alt="7 wireshark" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/21b04a36-d449-482e-b26e-e9288a59670c">

**Terminal:**

<img width="506" alt="7 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/07499aca-c1c2-4f39-ab81-00a7e95ee2a9">

## Explanation
For this question, we were asked the amout of packets that the **destination IP** is **184.87.193.88**. To get the amount of packets, I filtered it using ```ip.dst == 184.87.193.88``` on the **pcapng** file. After finished filtering, we can see at the bottom right that the amount of packets are ```6```.

# No. 8
## Question

# No. 9
## Question

# No. 10
## Question
> Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

**answer:** ```dhafin:kesayangannyak0k0```

**Wireshark:**

<img width="1440" alt="10 wireshark" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/1cfde359-a18b-4bb4-bb88-282a26285676">

**To get the username and password as the answer for the question:**

<img width="1440" alt="10 file jawaban" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/9e4ddd2d-afed-4847-b7b3-bdb28b61863b">

**Terminal:**

<img width="563" alt="10 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/7dde7bb3-b35b-42a1-a7f4-9786deb32049">

## Explanation
